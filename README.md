1) запрос(ы) для вставки данных минимум о двух книгах в коллекцию books

db.books.insertMany(
  [
      { title: "Заголовок книги 1", description: "Описание книги 1", authors: "Автор 1" },
      { title: "Заголовок книги 2", description: "Описание книги 2", authors: "Автор 2" },
      { title: "Заголовок книги 3", description: "Описание книги 3", authors: "Автор 3" }
  ]
);

2) запрос для поиска полей документов коллекции books по полю title

db.books.find( 
	{title: /.*книги.*/} 
);

3) запрос для редактирования полей: description и authors коллекции books по _id записи
 
db.books.updateOne(
	{_id: "531cc2410b4ebf000036b2d7"},
	{$set: {description: "Новое описание книги", authors: "Новый автор книги"}}
);
 