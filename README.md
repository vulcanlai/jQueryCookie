# jQueryCookie

* <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/1.11.1/jquery.js"></script>
* <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery-cookie/1.4.1/jquery.cookie.js"></script>

~~~
$(function () {
    function setCookie() {
        // set cookie 
        var expire_date = new Date();

        // 等待時間
        expire_date.setTime(expire_date.getTime() + (12 * 60 * 60 * 1000));

        $.cookie('ad-pall', 'Y', {
            path: '/',
            expires: expire_date
        });
    }

    var isCookie = $.cookie('ad-pall');
    if (isCookie !== 'Y') {
        // 執行 funtcion

        // 紀錄 cookie
        setCookie();
    }
})
~~~
