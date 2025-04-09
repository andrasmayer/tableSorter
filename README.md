import the required file<br>
tableSorter.js for ES6 module structure<br>
same for tableSorter.esm.min.js
tableSorter.min.js<br>
tableSorter.min.js is the standalone variant<br><br><br>




Usage:


const {tableSorter} = await import(`./dist/js/tableSorter.esm.min.js`) //For ES6 only
        
const data = [                                          //For data you can use array of (JSON) objects or a simple nested array
    {id:"1", name:"Ed", age:72, position:"Ceo"},
    {id:"2", name:"Tod", age:32, position:"Manager"},
    {id:"3", name:"Helen", age:27, position:"Slave"},
    {id:"4", name:"George", age:20, position:"Slave"},
    {id:"5", name:"Phil", age:44, position:"Slave"},
    {id:"6", name:"Pam", age:40, position:"Slave"},
    {id:"7", name:"Otto", age:41, position:"Slave"},
    {id:"8", name:"Julia", age:43, position:"Slave"},
    {id:"9", name:"Harmony", age:40, position:"Slave"},
    {id:"10", name:"Ted", age:37, position:"Slave"},
    {id:"11", name:"Matt", age:65, position:"Slave"},
    ]

const header = ["ID","Name","Age","Position"]

const table = new tableSorter({
    target : "#tableTarget",    //reference to the container you wanna put the table
    tableId : "table2",         //id for your table for later usage
    header : header,            //header array
    dataSet : data,             //data array 
    filters : [0,1,2,3],        //th indexes you wanna filter you can skip if you doesn't need em
    striped: true               //triped table. true/false or not using at all
})