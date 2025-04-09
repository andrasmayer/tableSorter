import the required file<br>
tableSorter.js for ES6 module structure<br>
same for tableSorter.esm.min.js
tableSorter.min.js<br>
tableSorter.min.js is the standalone variant<br><br><br>




Usage:<br><br>

const {tableSorter} = await import(`./dist/js/tableSorter.esm.min.js`) //For ES6 only<br><br>
        
const data = [                                          //For data you can use array of (JSON) objects or a simple nested array<br>
    {id:"1", name:"Ed", age:72, position:"Ceo"},<br>
    {id:"2", name:"Tod", age:32, position:"Manager"},<br>
    {id:"3", name:"Helen", age:27, position:"Slave"},<br>
    {id:"4", name:"George", age:20, position:"Slave"},<br>
    {id:"5", name:"Phil", age:44, position:"Slave"},<br>
    {id:"6", name:"Pam", age:40, position:"Slave"},<br>
    {id:"7", name:"Otto", age:41, position:"Slave"},<br>
    {id:"8", name:"Julia", age:43, position:"Slave"},<br>
    {id:"9", name:"Harmony", age:40, position:"Slave"},<br>
    {id:"10", name:"Ted", age:37, position:"Slave"},<br>
    {id:"11", name:"Matt", age:65, position:"Slave"},<br>
    ]<br><br>

const header = ["ID","Name","Age","Position"]<br><br>

const table = new tableSorter({<br>
    target : "#tableTarget",    //reference to the container you wanna put the table<br>
    tableId : "table2",         //id for your table for later usage<br>
    header : header,            //header array<br>
    dataSet : data,             //data array <br>
    filters : [0,1,2,3],        //th indexes you wanna filter you can skip if you doesn't need em<br>
    striped: true               //triped table. true/false or not using at all<br>
})<br><br>


Cell filters can listen to basic operators ( >, >=, <, <= ) Only when the column is numeric.<br>
For example >= 30 in the age cell returns everyone with 30yo or older<br>
Clicking on theads will sort the table alphabetically (asc/desc)<br>
You can add your custom CSS (see the examples).<br><br>
Throw a feedback to andrasmayer.github@gmail.com<br><br><br>
I will keep this project updated in the future
