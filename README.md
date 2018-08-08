# BDEEP Website

Our website based on a built-in domain at [Squarespace.com](https://www.squarespace.com/) and a third-party domain at [AWS](https://aws.amazon.com/). It contains four pages: About(Group intro), Team(intro), Research, and Contact. Website content including abstracts as well as key figures are crawled from [GitHub](https://www.github.com/uiuc-bdeep/Website/) and are updated automatically. Messages from Contact page will go directly to BDEEP group slack channel. Please visit [www.uiuc-bdeep.org](https://www.uiuc-bdeep.org/).

## Structure 
This repository includes two parts. One is [Code_files](https://github.com/uiuc-bdeep/Website/tree/master/Code_files) storing the HTML, CSS, JavaScript files that embeded in the website; the other is [Content_files](https://github.com/uiuc-bdeep/Website/tree/master/Content_files) keeping projects' content that show publicly.

```
Website
+--README.md
+--Code_files
|  +--About.html
|  +--Abstract.html
|  +--RecentPub.html
|  +--ProjectPage.html
|  +--Comment.html
+--Content_files
|  +--Public_Good_Complementarity
|  |  +--Abstract.tex(naming can be alternative)
|  |  +--key_figures
|  +--Environmental_Crises_Flint
|  |  +--Abstract.tex
|  |  +--key_figures
|  +--Speed_Reductions_Develop_City
|  |  +--Abstract.tex
|  |  +--key_figures
|  +--Housing_Discrimination
|  |  +--Abstract.tex
|  |  +--key_figures
|  +--Flood_Delay_Sao_Paulo
|  |  +--Abstract.tex
|  |  +--key_figures
|  +--Airbnb_Market
|  |  +--Abstract.tex
|  |  +--key_figures
```

## Modification Notes

* For those who edit website design</br>
`Abstract.html` : Crawling `Abstract.tex` and creating hover function for abstract on Research page</br>
`ProjectPage.html` : Crawling `key_figures` and presenting them in a slideshow mood, Like&Share button, full abstract</br>
`Comment.html` : Communicate website comment to slack channel #email</br>

* For those who edit project content</br>
`Abstract.tex`: Please check [How to commit changes on GitHub using ShareLaTeX](https://wiki.ncsa.illinois.edu/display/BDEEP/How+to+commit+changes+on+GitHub+using+ShareLaTeX) to synchronize your working paper from ShareLaTeX to your project folder. NOTE: Please keep the original format!</br>
`key_figures`: Please pick out figures that you want to show in the website and synchronize them to your project folder</br>

















