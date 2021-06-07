~~~js
setInterval(function () {
        let time = new Date();
        let h = time.getHours();
        let m = time.getMinutes();
        let s = time.getSeconds();
        hour.style.transform = `rotate(${
          h * 30 + (m / 60) * 30 + (s / 60 / 60) * 30
        }deg)`;
        min.style.transform = `rotate(${m * 6 + (s / 60) * 6}deg)`;
        sec.style.transform = `rotate(${s * 6}deg)`;
      }, 0);
~~~

