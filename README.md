social-js-api - это JS-обертка для использования ряда методов социальных сетей VKontakte, Facebook, Мой мир и Одноклассники.

Методы API

*  socialWrapper.getFriends
*  socialWrapper.getCurrentUser
*  socialWrapper.getAppFriends
*  socialWrapper.getProfiles
*  socialWrapper.inviteFriends
*  socialWrapper.resizeCanvas
*  socialWrapper.postWall
*  socialWrapper.makePayment

Методы:

*  socialWrapper.initResizeCanvas
*  socialWrapper.initContext
*  socialWrapper.getApiName

Для работы требуется jQuery.

		jQuery(document).ready(function() {
			var driverName = 'vk'; // или mm, или facebook: см resolveApiName в social-api.js
			var params = { mm_key: 'xxx', fb_id: 'xxx' }; // см example.html
			new SocialApiWrapper(driverName, params, callback);
		});

После выполнения будет доступен глобальный window.socialWrapper .

Реализовано приведение названий полей профиля пользователя к общему формату. Названия задаются так:

*  id
*  first_name
*  last_name
*  nickname
*  birthdate
*  gender
*  photo

В example.html - пример использования. Этот пример работает в четырех соц.сетях как iframe-приложение под такими адресами:

*  http://url.com/example.html?api=vk
*  http://url.com/example.html?api=mm
*  http://url.com/example.html?api=fb
*  http://url.com/example.html?api=ok

В Одноклассниках библиотека протестирована только в sandbox.

Здесь пока нет проверки пермишенов установленного приложения, это можно сделать в настройках приложения (VK, MM), или на сервере (FB).

Разработка начата, пока не стоит это использовать, api может измениться, и непременно изменится. Лучше участвуйте.

В планах - добавление полей профиля, авторизация с сайтов, обработка ошибок, обертка в deferred, много больше методов,
клиентская загрузка медиа-файлов, коллбеки для оплаты, и многое-многое другое.

