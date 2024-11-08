<div align="center" markdown>
<img src="https://i.imgur.com/wDdLM8H.png"/>


# Export to MOT

<p align="center">
  <a href="#Overview">Overview</a> •
  <a href="#How-To-Use">How To Use</a> •
  <a href="#Results">Results</a>
</p>

[![](https://img.shields.io/badge/supervisely-ecosystem-brightgreen)](https://ecosystem.supervisely.com/apps/supervisely-ecosystem/export-to-mot-format)
[![](https://img.shields.io/badge/slack-chat-green.svg?logo=slack)](https://supervisely.com/slack)
![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/supervisely-ecosystem/export-to-mot-format)
[![views](https://app.supervisely.com/img/badges/views/supervisely-ecosystem/export-to-mot-format.png)](https://supervisely.com)
[![runs](https://app.supervisely.com/img/badges/runs/supervisely-ecosystem/export-to-mot-format.png)](https://supervisely.com)

</div>

# Overview

App converts [Supervisely format](https://docs.supervisely.com/data-organization/00_ann_format_navi) project to [MOTChallenge format](https://motchallenge.net/) as **downloadable .tar archive**

<!-- In the modal window you have the option to export figures of all shapes or only figures with shape `Rectangle`. If project that you want to convert contains `None` type `tag` with name `ignore_conf` on video figures, result annotation will have `conf` value 0 for given figure. It means that this figure will not be considered for MOTChallenge framework evaluation. More about MOT format and `conf` value you can read [here](https://motchallenge.net/instructions/). All objects on video must have only one figure per frame. Backward compatible with [`Import MOT`](https://github.com/supervisely-ecosystem/import-mot-format) app. If you want to export video without figures select **Export all geometry shapes** in the modal window.

Current version of application supports only `gt` file annotations. -->

Application key points:  
- Supports only `gt` file annotations
- Backward compatible with [Import MOT](https://github.com/supervisely-ecosystem/import-mot-format)
- `ignore_conf` tag with type `None` sets `conf == 0` ([about conf](https://motchallenge.net/instructions/))



# How to Use
1. Add [Export to MOT](https://ecosystem.supervisely.com/apps/export-to-mot-format) to your team from Ecosystem.

<img data-key="sly-module-link" data-module-slug="supervisely-ecosystem/export-to-mot-format" src="https://imgur.com/XLOsIRN.png" width="350px" style='padding-bottom: 20px'/>  

2. Run app from the context menu of **Videos Project**:

<img src="https://imgur.com/Pda1KsZ.png" width="100%"/>

3. Select project export mode:  
- `Export all geometry shapes` — all object shapes (`polygon`, `bitmap`, etc.) will be converted to **rectangles**
- `Export only rectangle shapes`

<img src="https://imgur.com/aoCOox8.png" width="100%"/>


# Results

After running the application, you will be redirected to the `Tasks` page. Once application processing has finished, your link for downloading will be available. Click on the `file name` to download it.

<img src="https://i.imgur.com/4oE9sxi.png"/>

You can also find your converted project in   
`Team Files` -> `Convert Supervisely to MOT` -> `<taskId>_<projectId>_<projectName>.tar.gz`

<img src="https://i.imgur.com/3pDolxh.png"/>
