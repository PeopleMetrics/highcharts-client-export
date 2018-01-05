# highcharts-client-export

# Readme from the original highcharts-export-clientside project
Module for [HighCharts](http://www.highcharts.com/) to export charts client-side.

Webpage for this project is here: https://peoplemetrics.github.io/highcharts-client-export/

You may need to export a chart you made using HighCharts to an image or a PDF. It has an exporting module but it relies on an export server, which by default is http://export.highcharts.com/ and you also –unlucky you– have one or more of the following:
* your app doesn't have access to the intertubes;
* your chart contains sensitive data and you don't want an unsecure channel to carry it;
* sensitive data or not, you don't trust HighCharts with it;
* it's against your company policies;
* you don't want to set an export server up;
* you think it's 2015 and FFS, _browsers should be able to do that_.

Additionally, it provides a common interface between the official export module and `export-csv`.

## Documentation

Want to give it a try in your project? Check out [Github](https://peoplemetrics.github.io/highcharts-client-export/)
for installation instructions.

## Contribution

First, fork the project and clone it. Then, since dependencies are not shipped, so you will have to do the following:

```(sh)
bower install
```

Check the ```example.html``` file and mess with it. Once you are done, please consider making a pull request.

## Dependencies

This module depends on:
* [HighCharts](http://www.highcharts.com/) obviously, remember guys, it isn't free for commercial usages;
* its exporting module, that is bundle with it;
* for rasterized images (PNG, JPEG), a module called `canvas-tools` with is based<sup>1</sup> on [canvg](https://github.com/gabelerner/canvg) licenced under MIT Licence;
* [jsPDF](https://parall.ax/products/jspdf) (its GitHub page is [overthere](https://github.com/MrRio/jsPDF)) for PDF support, licenced under MIT Licence;
* Pseudo-official [export-csv](https://github.com/highslide-software/export-csv/tree/master) module for CSV and XLS support, under MIT Licence.

The only dependencies you must use are HighCharts and HighCharts exporting module. If you want PNG/JPEG, add `canvas-tools`. If you want PDF support, add both `canvas-tools` and `jsPDF`. If a dependency is missing for a file type, the option will not be available in the export menu.

<sup>1</sup> There are issues with canvg, title/subtitle appearing twice, this kind of things which `canvas-tools` fixes. So I'd suggest to go with this one.

## Changelog

### v1.0.0 - 2018-01-05

* Updated libs as needed
* ES6

## Next Up

* Updated Readme
* Code reduction where needed

## Credits

This is forked/rebased off of a now-abandoned `highcharts-export-clientside` by [A----](https://github.com/A----)  located on [GitHub](https://github.com/A----/highcharts-export-clientside)

