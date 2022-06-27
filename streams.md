# Информация о стримах

## Запрос на один стрим

GET /streams/{id}
где {id} = уникальный channelkey (он же в адресной строке)

## Ответ

{ Streams }

## Описание структур

Streams {  
 id :int // id стрима(чата)
 key :string // ключ-имя стрима
 preview :string // превьюшка стрима - ссылка на неё  
 title :string // название стрима  
 streamer :Streamer // объект описания стримера (уже указан в stream.md)
 streamKey :string // уникальный id-ключ строкой
 status :int // статус стрима 0 - оффлайн, 1- онлайн  
 game :Game // объект текущей игры  
 poster :string // ссылка на постер канала  
 hidden :boolean // "галка" - работает реверсивно  
 adult :boolean // галка 18+ работает реверсивно
 hosting :Streams  // информация о хостинге, если он сейчас активен. Поле не приходит, если стрим онлайн или оффлайн
 lastseen: int // время в UTС последнего запуска - не приходит, если стрим онлайн  
 premiums :int // число премиумов активных  
 followers :int // число фолловеров  
 rating :Rating // рейтинг стримера на сайте  
}

Game {  
 id :int // id игры в базе  
 title :string // название игры
 url :string // Видимо ссылка на игру так, как она записана (ключ)  
}

Rating {  
 value :int // число рейтинговых баллов  
 place :int // место в рейтинге стримеров  
}

Streamer {  
  id: int // уникальный id стримера  
  obj_key: string // ???  
  nickname: string // ник стримера на сайте  
  username: string // ник, обеспечивающий русские ники  
  avatar: string // ссылка на аватарку стримера  
}


## Запрос на все стримы

GET /streams

## Ответ

{ StreamList }

## Описание структур

StreamList {  
  streams[] :Streams // массив описания стримов  
  queryInfo :QueryInfo // информация о запросе на все стримы  
}

QueryInfo {  
  qty :int // ??? 
  page :int // число страниц в ответе  
  onPage :int // число стримов на 1 страницу  
}