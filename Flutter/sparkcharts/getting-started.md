---
layout: post
title: Getting started for Syncfusion Flutter Spark charts
description:  Learn how to create the Syncfusion Flutter Spark charts, add series, markers, data label, and trackball.
platform: flutter
control: Sparkline
documentation: ug
---

# Getting started with Flutter Spark charts

This section explains the steps required to populate the spark chart with data, data labels, marker and trackball. This section covers only the minimal features needed to know to get started with the spark charts.

## Add Flutter Sparkline Chart to an application

Create a simple project using the instructions given in the [Getting Started with your first Flutter app](https://flutter.dev/docs/get-started/test-drive?tab=vscode#create-app) documentation.

**Add dependency**

Add the Syncfusion Flutter Chart dependency to your pub spec file.

{% highlight dart %} 

    dependencies:

    syncfusion_flutter_charts: ^xx.x.xx

{% endhighlight %}

> **NOTE** 
Here **xx.x.xx** denotes the current version of [`Syncfusion Flutter Charts`](https://pub.dev/packages/syncfusion_flutter_charts/versions) package.

**Get packages**

Run the following command to get the required packages.

{% highlight dart %} 

    $ flutter pub get

{% endhighlight %}

**Import package**

Import the following package in your Dart code.

{% highlight dart %} 

    import 'package:syncfusion_flutter_charts/sparkcharts.dart';

{% endhighlight %}

## Initialize spark charts

Once the package has been imported, initialize the spark charts as a child of any widget. Here, as we are rendering Line chart, initialize [`SfSparkLineChart`]() widget as a child of Container widget.

{% highlight dart %} 

    @override
    Widget build(BuildContext context) {
        return Scaffold(
            body: Center(
                child: Container(
                    //Initialize spark charts
                    child: SfSparkLineChart()
                )
            )
        );
    }

{% endhighlight %}

## Bind data source

The [`data`]() property is used for binding data to the spark chart. This property takes the list value as input. 

{% highlight dart %} 

    @override
    Widget build(BuildContext context) {
        return Scaffold(
            body: Center(
                child: Container(
                    //Initialize chart
                    child: SfSparkLineChart(
                         data: <double>[
                             10,6, 8, -5, 11, 5, -2, 7, -3, 6, 8, 10
                         ]
                    )
                ),
            )
        );
    }

{% endhighlight %}

## Change the type of sparkline

You can change the sparkline type by setting the widget to [`SfSparkLineChart`](), [`SfSparkAreaChart`](), [`SfSparkBarChart`](), [`SfSparkLWinLossChart`](). Here, the sparkline type has been set to [`SfSparkAreaChart`]().

{% highlight dart %} 

    @override
    Widget build(BuildContext context) {
        return Scaffold(
            body: Center(
                child: Container(
                    //Initialize chart
                    child: SfSparkAreaChart(
                         data: <double>[
                             10,6, 8, -5, 11, 5, -2, 7, -3, 6, 8, 10
                        ]
                    )
                ),
            )
        );
    }

{% endhighlight %}

## Enable data label

You can add data labels to improve the readability of the chart using the [`labelDisplayMode`]() property.

{% highlight dart %} 

    @override
    Widget build(BuildContext context) {
        return Scaffold(
            body: Center(
                child: Container(
                    //Initialize chart
                    child: SfSparkLineChart(
                        //Enable data label
                        labelDisplayMode: SparkChartLabelDisplayMode.all,
                        data: <double>[
                            10,6, 8, -5, 11, 5, -2, 7, -3, 6, 8, 10
                        ]
                    )
                )
            )
        );
    }

{% endhighlight %}

## Enable trackball for sparkline

The sparkline displays additional information through trackball when touch the particular location to the sparkline. You can enable trackball by setting the [`trackball`]() property in [`SparkChartTrackball`](). Once it is activated, it will appear in the UI and move based on your touch movement until you stop touching on the chart.

{% highlight dart %} 

    @override
    Widget build(BuildContext context) {
        return Scaffold(
            body: Center(
                child: Container(
                    child: SfSparkLineChart(
                        //Enable the trackball
                        trackball: SparkChartTrackball(
                            activationMode: SparkChartActivationMode.tap
                        ),
                        data: <double>[
                            10,6, 8, -5, 11, 5, -2, 7, -3, 6, 8, 10
                        ]
                    )
                )
            )
        );
    }

{% endhighlight %}





