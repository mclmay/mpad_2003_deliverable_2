**October 31st 2026**<br>
**MPAD2003A Introductory Data Storytelling**<br>
**Makayla McLean**<br>
**Presented to Jean-Sébastien Marier**<br>

# Deliverable 2: Exploratory Data Analysis (EDA)

Use one hashtag symbol (`#`) to create a level 1 heading like this one. 

testing commits

## Foreword

For this assignment, you must clean and analyze the dataset from Deliverable 1, create exploratory charts/visualizations, and identify a potential story. Your assignment must clearly detail your process. You are expected to write about 1,000-1,200 words, and to include several screen captures showing the different steps you went through. Your assignment must be written with the Markdown format and submitted on GitHub.

I have been assigning different versions of this project to my digital journalism and data storytelling students for a few years now. Its structure was inspired by the main sections/chapters of [*The Data Journalism Handbook*](https://datajournalism.com/read/handbook/one/). This version was further inspired by the [Key Capabilities in Data Science](https://extendedlearning.ubc.ca/programs/key-capabilities-data-science) program offered by the University of British Columbia (UBC).

**Here are some useful resources for this assignment:**

* [GitHub's *Basic writing and formatting syntax* page](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
* [The template repository for this assignment in case you delete something by mistake](https://github.com/jsmarier/jou4100_jou4500_mpad2003_project2_template)

Did you notice how to create a hyperlink? In Markdown, we put the clickable text between square brackets and the actual URL between parentheses.

And to create an unordered list, we simply put a star (`*`) before each item.

## 1. Getting Data

## Why I chose this dataset:
I have chosen a dataset that includes the Location (address, postal code etc.) of cultural spaces that are considered natural around the city of Ottawa found on this page of Open Ottawa’s website: https://open.ottawa.ca/datasets/e68f322f9ccc4982ba8f973df4335158_137/explore?location=45.093626%2C-75.745170%2C0 . I chose this dataset because there are many ways to visualize this form of data such as visual maps, a navigable list or interactable map. I also decided to work with a dataset related directly to something I like and that I would personally find useful. It's also extremely important to inform people on the current environmental state and how these parks and green spaces affect our quality of life and overall quality of our city as a whole.

## General Observations of the dataset
There are 1022 rows and 49 columns in total within this dataset of which include the coordinates, official names and addresses of all the cultural nature spaces within Ottawa. Rows J and L have nominal variables J include the names of each park and L includes the addresses of all the parks in the city. There are quite a few empty cells as there are 3 rows for seasonal notes and general notes for both French and English though the majority are empty.. Rows F, AS, and AT are completely empty.

## how I imported the dataset
First I retrieved the dataset from the open ottawa database, then I downloaded the CSV file that was linked to the page. I then created a google sheets document to which I used the import option to open the CSV file within google sheets.




![](GoogleSheetsSS.png)<br>
*figure 1: Imported Google sheets screenshot* https://docs.google.com/spreadsheets/d/1mL5dRG-e_hPMJYjxaj1WzpE-BggnnTr5Zg7sfHNtjDs/edit?usp=sharing




Use two hashtag symbols (`##`) to create a level 2 heading like this one.

To include a screen capture, use the sample code below. Your images should be saved in the same folder as your `.md` file.

![](import-screen-capture.png)<br>
*Figure 1: The "Import file" prompt on Google Sheets.*

**Here are examples of functions and lines of code put in grey boxes:**

1. If you name a function, put it between "angled" quotation marks like this: `IMPORTHTML`.
1. If you want to include the entire line of code, do the same thing, albeit with your entire code: `=IMPORTHTML("https://en.wikipedia.org/wiki/China"; "table", 5)`.
1. Alternatively, you can put your code in an independent box using the template below:

``` r
=IMPORTHTML("https://en.wikipedia.org/wiki/China"; "table", 5)
```
This also shows how to create an ordered list. Simply put `1.` before each item.

## 2. Understanding Data

### 2.1. VIMO Analysis

Use three hashtag symbols (`###`) to create a level 3 heading like this one. Please follow this template when it comes to level 1 and level 2 headings. However, you can use level 3 headings as you see fit.

The dataset comes directly from the Open Ottawa website it only includes registered parks within the city of Ottawa, the page that the file is found explains that the data was collected by the apartment 613 community to create an updated inventory list of cultural spaces in Ottawa. 
After searching for the apartment 613 community on google i was met with multiple links of webpages and social media accounts related to or owned by the community. Apartment 613 is a community driven non-profit organization which focuses on sharing culture, foods, art, music, events, and more. 

Since there is such a large amount of rows and columns I could not properly cross check the exact locations and names of each park though when cleaning the data there were not many errors or duplicates. This data set is recent therefore it's not likely to be missing a park that was registered recently. 

All rows with Important information such as location (rows A, B, L, M, P, O, AH, and AI), Park name(rows J, and K), object ID (row C) are all fully filled in and don’t have any blank cells. The data seems to be properly filled out with accurate information. 

Rows F, AS, and AT are completely empty; they do not provide any further information.
Row F is simply the french version of row E they would be the same for both english and french. 


Support your claims by citing relevant sources. Please follow [APA guidelines for in-text citations](https://apastyle.apa.org/style-grammar-guidelines/citations).

**For example:**

As seen in Bounegru & Gray (2011), a data visualization should be clear...

### 2.2. Cleaning Data

To clean up the data set I started off by looking at the suggestions provided by google sheets once I imported the file. The google sheets cleanup tool found around 18 different cells with white space that could be trimmed down. I looked over the cells it flagged and accepted those of which needed the trimming. When looking for duplicates google sheets data cleaning tool did not find any duplicate cells. 
Open Refine edited a total of 49 cells when I selected the option of clearing and trimming out white spaces. 


### 2.3. Analyzing Data

Insert text here.

**This section should include a screen capture of your pivot table, like so:**

![](pivot-table-screen-capture.png)<br>
*Figure 2: This pivot table shows...*

**This section should also include a screen capture of your exploratory chart, like so:**

![](chart-screen-capture.png)<br>
*Figure 3: This exploratory chart shows...*

## 3. Delivering Data

Insert text here.

## 4. References

Include a list of your references here. Please follow [APA](https://apastyle.apa.org/style-grammar-guidelines/references) or [MLA](https://www.mla.org/MLA-Style) guidelines for references. Hanging paragraphs aren't required though.

**Here's an example:**

Bounegru, L., & Gray, J. (Eds.). (2021). *The Data Journalism Handbook 2: Towards A Critical Data Practice*. Amsterdam University Press. [https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153](https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153)
