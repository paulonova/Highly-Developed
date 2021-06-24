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

@using ClientDependency.Core.Mvc
@using ClientDependency.Core
@{
    Html.RequiresJs("~/scripts/Script1.js", 1);
    Html.RequiresJs("~/scripts/Script2.js", 2);

    Html.RequiresCss("~/css/style.css");
}
<html>
<head>
    @Html.RenderCssHere()
    @Html.RenderJsHere()
</head>

<hr>

## Partial Views

  <p>In Partial Views you can create block of Elements as Header, NavBars, Footer and then you can use everywhere adding @Html.Partial("name_of_partial_view")</p>



