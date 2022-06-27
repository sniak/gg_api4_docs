# Информация о стриме №1  

## Запрос: 

GET /stream/{id}
где {id} = уникальный channelkey (он же в адресной строке)

## Ответ:
{ Stream }

## Описание структур:

Stream {  
 id: int // уникальный id стрима  
 title: string // название стрима  
 link: string // ссылка на стрим  
 streamer: Streamer // структура  с описанием стримера  
 avatar: string // ссылка на аватарку стримера  
 hidden: string // стрим под галкой или нет  
 game: string // игра стрима  
 viewers: int // количество зрителей  
 preview: string // ссылка на ОЧЕНЬ маленькую превьюшку  
 poster: string // ссылка на превьюшку побольше  
 premium: int // премиум ли стример; 0 - нет, 1 - да  
 streamkey: string // id канала строкой  
 channelKey: string // Имя канала строкой  
 status : Boolean // Онлайн или оффлайн стрим  
 favorite: ??? // приходит null  
 source: Source // ссылки на m3u8 индексы разных качеств трансляций  
 obj_key: string // ????  
 gameUrl: string // игра стрима, по которой в базе учитывется?  
 online: int // Ещё один статус онлайна?  
 broadcast: Broadcast // информация о текущей трансляции; false, если оффлайн  
 hosting: Hosting // статус активного хоста; false, если оффлайн  
 last_online: string // время последней трансляции  
 stream_title: string // имя трансляции (снова)  
 cqty: string // ????  
 premiums: int // Число платных подписчиков  
 followers: int // Число фолловеров  
 allow_comments: int // Включены или нет комментарии под стримом  
 following: Boolean // Входит ли в число избранного у пользователя, что дёрнул ссылку  
 players: Players // описание плеера, там лежит лишь ГГшный  
}

Streamer {  
  id: int // уникальный id стримера  
  obj_key: string // ???  
  nickname: string // ник стримера на сайте  
  avatar: string // ссылка на аватарку стримера  
}

Broadcast {  
  start: int // время начала  
  game: string // название игры  
  title: string // название трансляции  
}

Players {  
  id: int // id плеера  
  title: string // название плеера  
  status: int // статус плеера (видимо онлайн/оффлайн)  
  server: int // расположение плеера по серверам  
}

Hosting {  
  obj_key: string // ????  
  id: int // уникальный id стрима  
  link: string // ссылка на стрим  
  preview: string // ссылка на ОЧЕНЬ маленькую превьюшку  
  poster: string // ссылка на превьюшку побольше  
  streamer: Streamer // структура с описанием стримера  
  game: string // игра стрима  
  gameUrl: string // игра стрима, по которой в базе учитывется?  
  viewers: int // количество зрителей  
  online: int // Ещё один статус онлайна?  
  broadcast: Broadcast // информация о текущей трансляции, в хосте пустая  
  hosting: Hosting // статус активного хоста  
  last_online: string // время последней трансляции  
  title: string // название стрима  
  stream_title: string // имя трансляции (снова)  
  cqty: string // ????  
  streamkey: string // id канала строкой  
  premium: int // премиум ли стример  
}
