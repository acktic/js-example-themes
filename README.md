# js-example-theme
Browser root attributes (customizable)

# example
let set = `Example`;

##
let themes = [
  { obFn: `Solarized`, class: `Solarized`, icon: `fa-digital-tachograph` },
];

##
for (i = 0; i <= themes.length - 1; i++) {
        (function (i) {
          document.addEventListener(
            `click`,
            function (event) {
              if (event.target.classList.contains(themes[i].class)) {
                window[themes[i].class]();
              }
            },
            false
          );
        })(i);
      }
