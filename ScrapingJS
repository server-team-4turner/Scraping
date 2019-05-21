/**
 * 
 */
const rp = require('request-promise');
const $ = require('cheerio');
//Published sheets website
const url = 'https://docs.google.com/a/my.cuhsd.org/spreadsheets/d/e/2PACX-1vQ4zNAaULxvhXdwDYP2Z8OFJY54V7TBadSDYIhXQSdwikZaf12u6T5pjiownwuT4-eq5CWSXavnhgGy/pubhtml';

rp(url)
  .then(function(html) {
    //success!
    const values = [];
    let count = 7;
    let s1 = 2;
    let s2 = 0;
    while(count < 210) {
   
      console.log($('th', html).siblings('td').eq(count).text());
      console.log($('th', html).siblings('.s1').eq(s1).text());
      console.log($('th', html).siblings('.s1').eq(s1 + 1).text());
      console.log($('th', html).siblings('.s2').eq(s2).text());
      console.log();
      
      count+=7;
      s1+=2;
      s2+=1;
    }
      
    /*
     * This line allows to read a selected cell from a table
     * $ is cheerio, 'th' is the table tag using html, siblings finds s0 classes or table cells, eq is 
     * the selected cell, and then it prints it in text
     * console.log($('th', html).siblings('.s0').eq(1).text());
    
    */
    
    //console.log($('td', html).text());
  })
  .catch(function(err) {
    //handle error
    console.log(err);
  });
