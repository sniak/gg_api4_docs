Запрос:  
GET /user/{id}  

Ответ:
{ ??? } 

Описание структур: 

??? { 
 admin :int // ???  
 user :User // объект пользователя  
 rights :string // Права пользователя  
 country :string // код страны по списку  
 city :string // код страны по списку  
 phone :string // номер телефона  
}

User {
 id : int // id пользователя  
 username :string // Имя пользователя  
 nickname :string // ник пользователя, отображается в чате, позволяет работать русским никам  
 avatar : string // ссылка на аватарку  
 icon :string // иконка, что отображалась раньше на форуме  
 iconId :int // id иконки  
 firstname :string // имя пользователя в профиле  
 lastname :string // фамилия пользователя в профиле  
 birthday :string // дата рождения пользователя в профиле  
 birthdayUTC :int // дата рождения в формате UTC  
 flag :string // флаг страны пользователя  
 country :string // страна пользователя строкой  
 timezone :string // временная зона по коду из списка  
 city :string // город пользователя, если пусто, то NULL  
 sex :int // пол пользователя 0 - мужской, 1 - женский, 2 - не указан  
 site :string // сайт пользователя, старое поле?  
 description :string // описание в профиле  
 image :string // ссылка на изображение фона  
 hide_adult :int // включено ли скрытие 18+ контента, сейчас скрыто  
 obj_key :string // какой-то код  
 online :boolean // онлайн ли пользователь  
 regDate :string // дата пользователя строкой  
 is_banned :boolean // забанен ли пользователь  
 privacy : Privace // права пользователя???  
}


Privacy {
 see_page :int //  
 priv_msg :int //  
 bio :int //  
 actions :int //  
 profile :int //  
}