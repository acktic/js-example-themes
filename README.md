# js-example-theme

Browser root attributes (customizable)

# example

let set = `Example`;

# use

`Light()`

## object Function
```
       let place = `js/themes/`;
       let type = `.js`;
      
let themes = [
  { obFn: `Light`, class: `Light`, icon: `fa-terminal` },
  { obFn: `Night`, class: `Night`, icon: `fa-code` },
];

for (i = 0; i <= themes.length - 1; i++) {
        theme = themes[i].obFn;
        let path = place + theme + type;
        let script = document.createElement(`script`);
        script.type = `text/javascript`;
        script.src = path;
        document.getElementsByTagName(`head`)[0].appendChild(script);
        if (set === theme)
          script.onload = (function () {
            let startup = setInterval(function () {
              setTimeout(function () {
                if (typeof eval(set) === `function`) {
                  window[set]();
                  clearInterval(startup);
                }
              }, 350);
            }, 500);
          })();
      }
```
