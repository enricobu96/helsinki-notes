---
attachments: [Clipboard_2021-09-16-17-10-52.png, Clipboard_2021-09-16-18-40-47.png, Clipboard_2021-09-16-18-47-01.png, Clipboard_2021-09-16-18-57-18.png, Clipboard_2021-09-16-19-11-10.png, Clipboard_2021-09-16-21-04-00.png, Clipboard_2021-09-16-21-24-14.png, Clipboard_2021-09-16-23-12-46.png, Clipboard_2021-09-16-23-33-41.png]
tags: [Introduction to Data Science]
title: Excercise 4 | Junk charts
created: '2021-09-16T13:44:38.913Z'
modified: '2021-09-16T20:48:08.521Z'
---

# Excercise 4 | Junk charts

## 4.1 - Junk charts

### Percent of Tornadoes vs Percent of Relate Deaths - 1950 to 1994

![](@attachment/Clipboard_2021-09-16-17-10-52.png)
Source: https://www.weatheronline.co.uk/reports/wxfacts/Fujita-Scale-Statistics.htm

This graph presents several problems: first thing first, the data-ink ratio. As well as being antiaesthetic, the tornado background is also a waste of ink: it does not provide any useful information, and rather it makes difficult to read and understand what the graph is trying to say.
The graphic also has redundant data: the y axis and the superimposed values are in fact the same. Furthermore, the legend could be useful, but it has no sense to report also the timespan.

### Food waste producing sectors

![](@attachment/Clipboard_2021-09-16-18-40-47.png)
Source: https://stopfoodwaste.ie/resources/business/food-waste-in-your-business

The main problem in this graph is the number of dimensions: while the data dimension is two (sector and percentage), this is a three dimensional graph, and the third dimension does not convey any information.

### Bubble Chart for Drug Samples

![](@attachment/Clipboard_2021-09-16-18-57-18.png)
Source: https://www.nist.gov/image/18for008bubblechartbackgroundlevelsjpg

The main problem in this chart is that it is difficult to infer the scale for every drug, since the reader should compare every point with the legend on the side. Another smaller problem are the horizontal lines superimposed on the graph, since they do not contribute in conveying information.

### Bonus: how (bad) data visualization can be used to manipulate masses

![](@attachment/Clipboard_2021-09-16-18-47-01.png)
Source: https://www.instagram.com/p/CTrazcMKoqE/

This chart was published 11/09/2021 on one of the most influential italian politicians, Matteo Salvini (the one on the center bar). To clarify, the translations of the texts are:
- Upper left: `Source: Ipsos (market research company) for Corriere della Sera (famous italian newspaper)`
- Botton: `Centre-right over 50%!`

The problem in this chart is trivial: in addition to not reporting the zero-point, the representation (i.e. both the length and the area of the bars) is not directly proportional to the number (a difference of 0.5% is many bigger than a difference of 1.2%).
I wanted to add also this chart to underline the power of data representation and the challenges it faces us; `With great power comes great responsibility`.

## 4.2 - Improved charts


### Percent of Tornadoes vs Percent of Relate Deaths - 1950 to 1994

![](@attachment/Clipboard_2021-09-16-21-24-14.png)

### Food waste producing sectors

![](@attachment/Clipboard_2021-09-16-23-12-46.png)

### Bubble Chart for Drug Samples

![](@attachment/Clipboard_2021-09-16-23-33-41.png)









