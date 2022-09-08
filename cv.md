# rsschool-cv

## Mikhailova Ekaterina

## Contact Info:

   * Email: katyamishha@gmail.com
   * telegram: @Katyamishha

## Summary

   I have been studying the development for about 7 years. 
   For the last 5 years I have been working in the web studio as a html converter. 
   I am given small tasks that I perform on jQuery. However, I want more development, 
   I want to be good at JavaScript.

## Skills

   * Convert PSD to HTML (with bootstrap, uikit, jade, SCSS, mobile friendly);
   * HTML Email;
   * Basics of JavaScript;
   * jQuery;
   * Little experience Vue, Node.js;

## Code examples

   *It was necessary to parse information from the site, 
    difficulties arose in the process, because the site noticed suspicious
    activity and asked for a captcha*

   ```javascript
        var request = require("request"),
        cheerio = require("cheerio"),
        fs = require('fs'),
        url = "https://tld-list.com/tlds-from-a-z";

        request(url, function(error, response, body) {
        if (!error) {
                var $ = cheerio.load(body),
                reg_number = $(".text-left > a");
                links = Array.from(reg_number.map(function(index, element) {
                return {
                        domain: element.childNodes[0].nodeValue,
                        link: element.attribs['href']
                };
                }));
                if (links.length > 0) {
                var itogJson = JSON.stringify(links, null, 4);
                fs.writeFileSync("domains.json", itogJson);
                return;
                } else {
                error = "сайт заблокирован";
                }
        }
        console.log("Произошла ошибка: " + error);

        });
```

## Experience

I work in web studio, here are some of my recent work.
  
  * [Архитектурное бюро](https://nosorogdesign.ru/)
  * [Производственное предприятие](https://prestige-holding.ru/)
  * [Этот я делала на vue.js](https://infra-site.ru/quiz)

## Education

Master's degree in Engineering and Technology (not related to iT).

## English 

A1