# Highly-Developed Umbraco Project
<hr>

## &#9762; Umbraco Documentation

• Settings  => Datatype: You can configurate all templates in Umbraco, ex: textarea, radiobox, even the Document Types.

### &#9818; Insert new Data type in a Document Type:
<ul>
  <li>Create a Data type.</li>
  <li>Go to Document type</li>
  <li>Select the document type you wish</li>
  <li>Add new property</li>
  <li>Select my new Data type</li>
  <li>Save</li>
</ul>
<br>

### &#9818; Create a New Document Type:

<ul>
  <li>Go to Settings and create a new Document Type</li>
  <li>Select the Document you wish to add the new Document type. ex: Home, Blog, Contact, etc..</li>
  <li>Click in Permission and add the new Document type.</li>
  <li>Then you can go to Content and select (3 points) to create a new Content.</li>
  <li>You will see your New Document Type available.</li>
</ul>

### &#9818; DEBUG: https://localhost:44301/?umbDebug=true   start a Debug mode..
<br/>

<hr>

### &#9818; MVC & Permissions

#### Model:   Document type
#### View:  Content => Templates + views
#### Controller => Umbraco handle this


### &#9818; Permissions:

#### Create a Document type
#### Create a Template to this Doc Type
#### Set PERMISSION to "Allow as a Root" 


### &#9818; Design Process

<ul>
  <li>Sketch => One Note</li>
  <li>Wireframe => Balsamic or InVision</li>
  <li>Review => PowerPoint</li>
  <li>Design => CorelDraw, Photoshop</li>
</ul>
<br>


### &#9818; Compositions - Inheritence

#### Create a Document Type (it will be a model)
#### Set in Permitions as an Element Type.  ps: Never create this Document type in the Content tree.
#### In each page, click in COMPOSITION button and add the new Element Type.
#### Go to Templates and add the @Model.Value("id-from- theelement");
#### Go to Content and set the values in the new Element type.
<br>

### &#9818; CDF - Client Dependency Framework

https://our.umbraco.com/Documentation/Fundamentals/Design/Stylesheets-Javascript/

<code>@using ClientDependency.Core.Mvc</code><br>
<code>@using ClientDependency.Core</code><br>
<code>@{</code><br>
<code>Html.RequiresJs("~/scripts/Script1.js", 1);</code><br>
<code>Html.RequiresJs("~/scripts/Script2.js", 2);</code> <br>
<code> Html.RequiresCss("~/css/style.css");</code><br>
<code>}</code><br>
<code><html></code><br>
<code><head></code><br>
<code> @Html.RenderCssHere()</code><br>
<code>@Html.RenderJsHere()</code><br>
<code></head></code><br>

<hr>

## Partial Views

  <p>In Partial Views you can create block of Elements as Header, NavBars, Footer and then you can use everywhere adding @Html.Partial("name_of_partial_view")</p>

  
  ### &#9818; Call to Action  => Multi Url Picker
  
  Link to Source: https://our.umbraco.com/Documentation/Fundamentals/Backoffice/property-editors/Built-in-Property-Editors/Multi-Url-Picker/


### &#9818; List of Articles
  
  <ul>
    <li>Create a Single Article (Document Type)</li>
    <li>Set all elements you need: Name, Date, Comments, Image ...</li>
    <li>Then Create a Container for all Single Articles (Document Type)</li>
    <li>Set as a List View</li>
    <li>In Permissions add Single Article as a Child</li>
    <li>In Home (document type) in Permissions, allow to create a Container For Articles</li>
    <li>Go to Content and Create under Home a new Content "Article List"</li>
    <li>Click in this new "Article List" and a Button to create New Articles will apear</li>
    <li>Create a New Article</li>
    <li>*** To Make the Article Visible ***</li>
    <li>Go to Home in Templates</li>
    <li>Select "Query Builder" to get the query for the Artcles</li>
    <li>Loop throw all Articles and display the contents</li>
    <li>Then, you can transfer the code and create a Partial View</li>    
  </ul>
  
  <hr>
  
  ## Umbraco Navi Hide => To hide pages in NavBar
  
  <ul>
    <li>Create a Document Type named "Navigation"</li>
    <li>Set Properti as Checkbox (true/false) whith name "Umbraco Navi Hide"</li>
    <li>Go to Content Page and  add as a Composition</li>
    <li>Go to the site you want to hide and check as true</li>
    <li>Go to Partial Views NavBar.cshtml</li>
    <li>Add the code:  @foreach(var page in homePage.Children.Where(w => w.IsVisible())){</li>
    <li>Save</li>
  </ul>
  
 
  ## Nested Content
  
  <ul>
     <li>Create a Document Type without template</li>
     <li>Set then as an Element Type</li>
     <li>Set the fields (Link Text, Link Icon <fontawesome>, Link Url</li>
     <li></li>
     <li></li>
     <li></li>
  </ul>
  
  
