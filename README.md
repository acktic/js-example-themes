# js-example-theme
Browser root attributes (customizable)

# example
let set = `Example`;

##
let themes = [
  { obFn: `Solarized`, class: `Solarized`, icon: `fa-digital-tachograph` },
];

##
for (i = 0; i <= themes.length - 1; i++) {<br>
        (function (i) {<br>
          document.addEventListener(<br>
            `click`,<br>
            function (event) {<br>
              if (event.target.classList.contains(themes[i].class)) {<br>
                window[themes[i].class]();<br>
              }<br>
            },<br>
            false<br>
          );<br>
        })(i);<br>
      }
