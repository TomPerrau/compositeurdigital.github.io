# Web Pages

This content allows you to display a local html content, or a web site page inside your Compositeur Digital UX. Web site pages can also be displayed as links, so that when they are selected, an external web browser is showing them.

To interact with a web page, press the navigation button at the center of the item: it starts the navigation mode.

![Web page navigation mode enabled](../../img/content_web_page_start.JPG)

In navigation mode, slide your finger on the item to rotate the camera and see the scene. If you don't touch the web page for 10 seconds in navigation mode, it will automatically disable the navigation mode and your item will behave normally when you touch it. You can also press the `end navigation` button (next to the action button) to end navigation.

![Web page navigation mode disabled](../../img/content_web_page_end.JPG)

## Action within Compositeur Digital UX

Web page items support the following action. To have a complete overview of each action, [see the section Actions](actions.md)

**Actions menu**

| Annotate | Capture  | Duplicate | Save as  | Selection | Share    | 
|:--------:|:--------:|:---------:|:--------:|:---------:|:--------:|
| &#x2716; | &#x2716; | &#x2714;  | &#x2716; | &#x2714;  | &#x2716; |

**Interaction with the item**

| Navigation Mode | Web page navigation |
|:---------------:|:--------------------|
| &#x2714;        | &#x2714;            |

## Content extensions

Depending on your goal, you have several content extensions which can be used.

### I want to display a web site link which will be opened in a web browser

To display a web site link which will be opened in a web browser, create a file named `<NameOfMySite>.cdurl`. Inside this file, add a line :
`url = <UrlOfMyWebsite>`,  e.g, `url = https://www.msn.com/en-us/`

![Web browser link](../../img/content_web_page_link_folder.JPG)

### I want to display an external web site inside my Compositeur Digital UX

To display a web site inside your Compositeur Digital UX, you need a `.cdurl` file, and a `meta` file. Metadata are very useful to customize the way your Compositeur Digital UX acts. [Check the metadata section for more information](../advanced_setting.md).

Create a file named `<NameOfYourCdurlFile>_meta.txt`,  e.g., i have a `.cdurl` file named `msn.cdurl`, my meta file should be named `msn_meta.txt`.

Inside this meta file, add a line : `table.viewer = cdux`.
With this line, the web page will be opened inside your Compositeur Digital UX.

![Compositeur Digital UX Web viewer](../../img/content_web_page_cdux_folder.JPG)

### I want to display local HTML content

To display local HTML content, create a folder and add the extension `.html` or `.web` at the end of the name of your folder. Inside your `web` folder, you can use `css`, `htm`, `html` and `js` files. You can use images as well.

If you have several `html` files inside this folder, by default, Compositeur Digital UX will look for a file named `index.hmtl`. If no such file can be found, the starting file will be the first regarding the alphabetical order.

![Local HTML content](../../img/content_web_page_local_folder.JPG)

### Summup

|          | Web site link (web browser) | Web site (CDUX)   | Local Html content       |
|----------|:----------------------------|:------------------|:-------------------------|
|Extensions| `cdurl`                     | `cdurl` + `_meta` | Folder `.html` or `.web` |

## Metadata available

Metadata will help you to customize the way your web viewer behaves.

| Metadata Key                      | Value               | Description                                                               |
|:---------------------------------:|:-------------------:|:--------------------------------------------------------------------------|
| `table.viewer`                    | cdux                | Makes sure the `cdurl` link will be displayed inside Compositeur Digital UX |
| `web.manipulationMode`            | 1 or 0              | If 1, the user will have to enable navigation mode, then the view will behave like a browser. If 0, the navigation mode will be reduced. |
| `web.showChrome`                  | True of False       | If true, a navigation bar at the top of the view will be shown. Else, no navigation bar will be displayed. |
| `web.viewport.width`              | 1000 (number)       | Sets the default width of the view.                                       |
| `web.viewport.height`             | 800 (number)        | Sets the default height of the view.                                      |

By default , `cdurl` link have the metadata `web.manipulationMode` set to 1 and the metadata `web.showChrome` set to True.

Folders with the extension `.web` or `html` have the metadata `web.manipulationMode` set to 0 and the metadata `web.showChrome` set to False.

Navigation Mode to 1 (left) and 0 (right)

![Navigation mode 1 (left) vs 0 (right)](../../img/content_web_page_manipulationMode.JPG)

ShowChrome True (left) and ShowChrome False (right)

![ShowChrome true (left) vs false (right)](../../img/content_web_page_showChrome.JPG)

## Download a sample

A Demo Universe which contains samples for web page contents is available, [give it a try!](../Demo-Universe.zip) &#x1f604;

Next : [Creating Templates](templates.md)
