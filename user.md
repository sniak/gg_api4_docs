# Информация о пользователе

## Запрос

GET /user/{id}  

## Ответ

{ UserInfo }

## Описание структур

UserInfo {  
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

# Информация со стримом

## Запрос

GET /user/{id}/view  

## Ответ

{ UserView }  

## Описание структур

UserView {  
 user :User // Объект пользователя  
 stream : StreamView // Объекст стрима обрезанный  
}

## Описание структур

StreamView {  
 id: int // уникальный id стрима  
 title: string // название стрима  
 link: string // ссылка на стрим  
 streamer: Streamer // структура  с описанием стримера  
 avatar: string // ссылка на аватарку стримера  
 hidden: string // стрим под галкой или нет  
 game: GameView // игра стрима  
 viewers: int // количество зрителей  
 preview: string // ссылка на ОЧЕНЬ маленькую превьюшку  
 poster: string // ссылка на превьюшку побольше  
 premium: int // премиум ли стример; 0 - нет, 1 - да  
 streamkey: string // id канала строкой  
 channelKey: string // Имя канала строкой  
 status : Boolean // Онлайн или оффлайн стрим  
 favorite: ??? // приходит null  
 source: Source // ссылки на m3u8 индексы разных качеств трансляций  
}

GameView {  
 id :string // id игры строкой  
 poster :string // постер игры ссылка, скорее всего пусто  
 poster3d :string // ???
 title :string // название игры строкой
 url :string // Видимо ссылка на игру так, как она записана (ключ)  
}