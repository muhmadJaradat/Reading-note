#  Chart.js, Canvas

Charts are far better for displaying data visually than tables and have the added benefit that no one is ever going to press-gang them into use as a layout tool. They’re easier to look at and convey data quickly, but they’re not always easy to create.

A great way to get started with charts is with Chart.js, a JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page. It’s a well documented plugin that makes using all kinds of bar charts, line charts, pie charts and more, incredibly easy.

## Setting up

The first thing we need to do is download Chart.js. Copy the Chart.min.js out of the unzipped folder and into the directory you’ll be working in. Then create a new html page and import the script:

``` <!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Chart.js demo</title>
        <script src='Chart.min.js'></script>
    </head>
    <body>
    </body>
</html> 
```

## Drawing a line chart

To draw a line chart, the first thing we need to do is create a canvas element in our HTML in which Chart.js can draw our chart. So add this to the body of our HTML page:

``` <canvas id="buyers" width="600" height="400"></canvas> ```

Next, write a script that will retrieve the context of the canvas, so add this to the foot of your body element:

``` <script>
    var buyers = document.getElementById('buyers').getContext('2d');
    new Chart(buyers).Line(buyerData);
</script>
```

(We can actually pass some options to the chart via the Line method, but we’re going to stick to the data for now to keep it simple.)

Inside the same script tags we need to create our data, in this instance it’s an object that contains labels for the base of our chart and datasets to describe the values on the chart. Add this immediately above the line that begins ‘var buyers=’.

## Installation

You can download the latest version of Chart.js from the GitHub releases or use a Chart.js CDN. Detailed installation instructions can be found on the installation page.

## Creating a Chart

t's easy to get started with Chart.js. All that's required is the script included in your page along with a single `<canvas>` node to render the chart.

In this example, we create a bar chart for a single dataset and render that in our page. You can see all the ways to use Chart.js in the usage documentation.

``` <canvas id="myChart" width="400" height="400"></canvas>
<script>
var ctx = document.getElementById('myChart').getContext('2d');
var myChart = new Chart(ctx, {


    type: 'bar',


    data: {
        labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],


        datasets: [{


            label: '# of Votes',

            data: [12, 19, 3, 5, 2, 3],


            backgroundColor: [


                'rgba(255, 99, 132, 0.2)',


                'rgba(54, 162, 235, 0.2)',


                'rgba(255, 206, 86, 0.2)',


                'rgba(75, 192, 192, 0.2)',


                'rgba(153, 102, 255, 0.2)',


                'rgba(255, 159, 64, 0.2)'


            ],


            borderColor: [


                'rgba(255, 99, 132, 1)',


                'rgba(54, 162, 235, 1)',


                'rgba(255, 206, 86, 1)',


                'rgba(75, 192, 192, 1)',


                'rgba(153, 102, 255, 1)',


                'rgba(255, 159, 64, 1)'


            ],
            borderWidth: 1


        }]
    },

    
    options: {


        scales: {


            yAxes: [{


                ticks: {


                    beginAtZero: true
                }
            }]
        }
    }
});


</script> 
```

