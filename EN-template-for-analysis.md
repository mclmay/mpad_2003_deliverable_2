**October 31st 2026**<br>
**MPAD2003A Introductory Data Storytelling**<br>
**Makayla McLean**<br>
**Presented to Jean-Sébastien Marier**<br>

# Deliverable 2: Exploratory Data Analysis (EDA)

## Foreword

For this assignment, you must clean and analyze the dataset from Deliverable 1, create exploratory charts/visualizations, and identify a potential story. Your assignment must clearly detail your process. You are expected to write about 1,000-1,200 words, and to include several screen captures showing the different steps you went through. Your assignment must be written with the Markdown format and submitted on GitHub.

I have been assigning different versions of this project to my digital journalism and data storytelling students for a few years now. Its structure was inspired by the main sections/chapters of [*The Data Journalism Handbook*](https://datajournalism.com/read/handbook/one/). This version was further inspired by the [Key Capabilities in Data Science](https://extendedlearning.ubc.ca/programs/key-capabilities-data-science) program offered by the University of British Columbia (UBC).

**Here are some useful resources for this assignment:**

* [GitHub's *Basic writing and formatting syntax* page](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
* [The template repository for this assignment in case you delete something by mistake](https://github.com/jsmarier/jou4100_jou4500_mpad2003_project2_template)

Did you notice how to create a hyperlink? In Markdown, we put the clickable text between square brackets and the actual URL between parentheses.

And to create an unordered list, we simply put a star (`*`) before each item.

## Why I chose this dataset:
I have chosen a dataset that includes the Location (address, postal code etc.) of cultural spaces that are considered natural around the city of Ottawa found on this page of Open Ottawa’s website:https://open.ottawa.ca/datasets/e68f322f9ccc4982ba8f973df4335158_137/explore?location=45.093626%2C-75.745170%2C0 . I chose this dataset because there are many ways to visualize this form of data such as visual maps, a navigable list or interactable map. I also decided to work with a dataset related directly to something I like and that I would personally find useful. It's also extremely important to inform people on the current environmental state and how these parks and green spaces affect our quality of life and overall quality of our city as a whole.

## General Observations of the dataset
I think columns E, D and C contain the most important information that I should use to create my data driven story. Column D contains nominal variables with the names of each park. Column E also contains nominal variables with the addresses of the parks. Column C also contains nominal variables, specifically categorical nominal variables with the tags for each park. After observing these specific columns the question of how can creating a story using the locations of parks be more helpful than just simply googling the location yourself came to mind. 

## how I imported the dataset
First I retrieved the dataset from the open ottawa database, then I downloaded the CSV file that was linked to the page. I then created a google sheets document to which I used the import option to open the CSV file within google sheets.

![](GoogleSheetsSS.png)<br>
*figure 1: image of Google sheets document after CSV file has been imported* https://docs.google.com/spreadsheets/d/1mL5dRG-e_hPMJYjxaj1WzpE-BggnnTr5Zg7sfHNtjDs/edit?usp=sharing




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
I have chosen to conduct my VIMO analysis on the columns E, D and C. 
Column D contains the names of all the parks there are a total of 1022 unique values  including the title cell there are no empty cells and all contain valid unique park names to match those of the one within the city of Ottawa. I am unable to properly cross check the names of every park. 
Column E contains the addresses of each park in the city of Ottawa, there are a total of 1022 rows and 261 unique values. There are a total of 16 values labeled as N/A and exactly one empty cell. I am unable to properly cross check each location, there are a few locations that are listed multiple times. Figure 4 shows the information that is given when selecting the "columns stats” under the “data” category at the top of the page on google sheets.

![](Figure4.png)<br>

The last column I chose to conduct a VIMO analysis on is column C which contains the tags connected to each park. There are a total of 1022 rows and a total of 50 unique values. 958 of those values are “park” ; the tags that are listed contain valid types of cultural spaces in the natural category such as “parks, university”, “swimming”, “Heritage, rural, agriculture, conservation”, etc. Figure 5 shows the information that is given when selecting the "columns stats” under the “data” category at the top of the page on google sheets. 

![](Figure5.png)<br>

Support your claims by citing relevant sources. Please follow [APA guidelines for in-text citations](https://apastyle.apa.org/style-grammar-guidelines/citations).

**For example:**

As seen in Bounegru & Gray (2011), a data visualization should be clear...

### 2.2. Cleaning Data

When cleaning the data there were not many errors or duplicates. This data set is recent therefore it's not likely to be missing a park that was registered recently. 
All rows with Important information such as location (rows A, B, L, M, P, O, AH, and AI), Park name(rows J, and K), object ID (row C) are all fully filled in and don’t have any blank cells. The data seems to be properly filled out with accurate information. 
I started off by removing the french version of each column as it contains the same information as the english columns. I then removed all empty columns and those of which I will not be using for my data driven story. 
To clean up the data set I started off by looking at the suggestions provided by google sheets once I imported the file. The google sheets cleanup tool found around 18 different cells with white space that could be trimmed down. I looked over the cells it flagged and accepted those of which needed the trimming. When looking for duplicates google sheets data cleaning tool did not find any duplicate cells. I then used the function `=E1:E1022 & " " & F1:F1022` to combine columns E and F together into one. 
Open Refine edited a total of 49 cells when I selected the option of clearing and trimming out white spaces. In comparison to google sheets which only found 18 cells with white spaces that needed to be trimmed.

### 2.3. Analyzing Data

The dataset comes directly from the Open Ottawa website it only includes registered parks within the city of Ottawa, the page that the file is found explains that the data was collected by the apartment 613 community to create an updated inventory list of cultural spaces in Ottawa. 
After searching for the apartment 613 community on google I was met with multiple links of webpages and social media accounts related to or owned by the community. Apartment 613 is a community driven non-profit organization which focuses on sharing culture, foods, art, music, events, and more. I chose to focus on keeping the locations and names of all the parks whether their active what and category of cultural space they are to help make my potential map useful for people who are looking for a park that is within a specific category. 
I created a pivot table to help only show the most important information that I would require to make my data driven story. I included the location names, addresses, activity status, category, etc. these will be used to create the visual map of the locations of the parks within the city. 
![](PivotTableSS.png)<br>
*Figure 2: this pivot table shows rows A to J and up to column 41, containing the x,y coordinates, category, name, address, city, province,sub category, and postal code listed in the original dataset.*
For my exploratory chart I created a chart that shows the active status for all the parks in the data set. This is important because it shows how many of the parks are active, which shows that currently all 1021 parks are active. 
![](ACTIVE-PARKS.png)<br>
*Figure 3: this exploratory chart shows all the parks activity status, 1021 parks total are currently active in Ottawa.*


## 3. Delivering Data
For this story I would have to do some research on the impacts of parks and natural spaces on the community and ecosystem/environment of the city. Along with this I would also benefit from doing general research on how parks can improve quality of life and its environmental impacts.

On the story section of the about us page on the apartment 613 website it explains that: Apartment 613 was established in 2008 and the next year, 2009 the official website was launched. This organization was started by a group of friends who wanted to create an easier way to “tap into Ottawa’s vibrant arts and culture scene without insider connections” too which now is a full-fledged organization that helps bring the Ottawa community together to experience Ottawa's arts and culture scene. Interviewing someone who helped collect the data or works within the apartment 613 organization would be a great opportunity to learn about why they thought creating an inventory of cultural spaces was important and how they personally think it could be used to better our city. By hearing their intentions I could help them put that into motion within my data story. They could also explain how they retrieved the data, how long the data took to be collected, and if there are any changes that should be made to it. Apartment 613 is widely run by volunteers who publish their stories or provide information about events around Ottawa. Speaking with someone who is an active contributor would be a great way to discuss ideas on how to work with this data to create a visual story that would help the public be able to find and access cultural spaces easily. 



## 4. References

Include a list of your references here. Please follow [APA](https://apastyle.apa.org/style-grammar-guidelines/references) or [MLA](https://www.mla.org/MLA-Style) guidelines for references. Hanging paragraphs aren't required though.

**Here's an example:**

Bounegru, L., & Gray, J. (Eds.). (2021). *The Data Journalism Handbook 2: Towards A Critical Data Practice*. Amsterdam University Press. [https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153](https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153)
