# Text-Mining-and-Web-Scrapping

Text data falls into the category of unstructured data and requires some preparation before it can be used for modeling. Text preparation is different from structured data pre-processing.

We will walk through the process of preparing text data and building a predictive model on it.

# Topic Modeling
Topic Modeling automatically discover the hidden themes from given documents. It is an unsupervised text analytics algorithm that is used for finding the group of words from the given document. These group of words represents a topic. There is a possibility that, a single document can associate with multiple themes.

# Comparison Between Text Classification and Topic Modeling
Text classification is a supervised machine learning problem, where a text document or article classified into a pre-defined set of classes. Topic modeling is the process of discovering groups of co-occurring words in text documents. These group co-occurring related words makes "topics". It is a form of unsupervised learning, so the set of possible topics are unknown. Topic modeling can be used to solve the text classification problem. Topic modeling will identify the topics presents in a document" while text classification classifies the text into a single class.

# Use Cases of Topic Modeling
Simple applications in which this technique is used are documented clustering in text analysis, recommender systems, and information retrieval. More detailed use-cases of topic modeling are:

Resume Summarization: It can help recruiters to evaluate resumes by a quick glance. They can reduce effort in filtering pile of resume.


Search Engine Optimization: Online articles, blogs, and documents can be tag easily by identifying the topics and associated keywords, which can improve optimize search results.


Recommender System Optimization: Recommender systems act as an information filter and advisor according to the user profile and previous history. It can help us to discover unvisited relevant content based on past visits.


Improving Customer Support: Discovering relevant topics and associated keywords in customer complaints and feedback for examples product and service specifications, department, and branch details. Such information help company to directly rotated the complaint in respective department.

# A Small Introduction to Hyper Text Markup Language (HTML)
Hypertext Markup Language is the standard markup language for documents designed to be displayed in a web browser. It can be assisted by technologies such as Cascading Style Sheets(CSS) and scripting languages such as JavaScript(JS).

HTML describes the structure of a Web page
HTML consists of a series of elements
HTML elements tell the browser how to display the content
HTML elements are represented by tags
HTML tags label pieces of content such as "heading", "paragraph", "table", and so on
Browsers do not display the HTML tags, but use them to render the content of the page
Simple HTML document code to be added
The declaration defines this document to be HTML5
The < html> element is the root element of an HTML page
The < head> element contains meta information about the document
The < title> element specifies a title for the document
The < body> element contains the visible page content
The < h1> element defines a large heading
The < p> element defines a paragraph
HTML Tags
HTML tags are element names surrounded by angle brackets

Example: < tagname>content goes here...</ tagname>

HTML tags normally come in pairs like < p> and < /p>
The first tag in a pair is the start tag, the second tag is the end tag
The end tag is written like the start tag, but with a forward slash inserted before the tag name
HTML Page Structure

Most Commonly Used Tags
Div tag: div tag is used as a container to represent an area on the screen.

Anchor tag: It is used to link one page to another page.
< a href="..."> Statements... < /a>

List tag: It is used to list the content.
< li> Statements... < /li>

Ordered List tag: It is used to list the content in a particular order.
< ol> Statements... < /ol>

< ol>

  < li>List item 1< /li>  
  < li>List item 2< /li> 
  < li>List item 3< /li>  
  < li>List item 4< /li>  
< /ol>

Unordered List tag: It is used to list the content without order.
< ul> Statements... < /ul>

< ul>

  < li>List item 1< /li>  
  < li>List item 2< /li> 
  < li>List item 3< /li>  
  < li>List item 4< /li>  
< /ul>

Image tag: It is used to add image element in html document.
< img src="" width="40" height="40" >

Tables Tags: Table tag is used to create a table in html document.

  < table> 
    < tr> 
      < th>Month< /th> 
      < th>Savings< /th> 
    < /tr> 
    < tr> 
      < td>January< /td> 
      < td>100< /td> 
    < /tr> 
   < /table>

Th tag: It defines the header cell in a table.
Tr tag: It is used to define row of html table.
Td tag: It defines the standard cell in html document.
Form tag: It is used to create html form for user.
Submit input tag: It is used to take the input from the user.

    < form method=post action="/cgibin/example.cgi"> 
        < input type="text" maxlength="30">  
        < input type="Submit" value="Submit">  
    < /form>
# Web Scraping with BeautifulSoup
This activity will use the below modules:

Requests: To make web requests

Beautiful Soup: To extract data from the HTML response

BeautifulSoup can extract single or multiple occurrences of a specific tag and can also accept search criteria based on attributes such as:

Find: This function takes the name of the tag as string input and returns the first found match of the particular tag from the webpage response

Findall: Use find_all to extract all the occurrences of a particular tag from the page response.
find_all returns an object of ResultSet which offers index based access to the result of found occurrences and can be printed using a for loop.
find_all can accept a list of tags as soup.find_all(['th', 'td']) and parameters like id to find tags with unique id

Select: This function finds multiple instances and returns a list.

Attribute Driven Search: Most of the times attributes like id, class, or value are used to further refine the search. 
Example soup.find_all('table')

Nested Tags: Nested tags can be found using the select method.
Example: soup.select("html head p")[0].get_text()


Beautiful Soup also provides navigation properties like

next_sibling and previous_sibling: To traverse tags at same level, like tr or td within the same tag.

next_element and _previouselement: To shift HTML elements.


Points To Remember: 

The logic to extract the data usually depends upon the HTML structure of the webpage, so some changes in structure can break the logic.

The content of a website can be subject to applied laws, so make sure to read the terms and conditions about content

Problem Statement: Determining the Latent Topics from blogs
First Level Extraction
Extracting all Authors and their corresponding blog links at level 1:

https://indianbloggers.org/
