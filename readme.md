# What does this script do?

This script makes it quick and easy to add Google Analytics Event Tracking to your HTML links. This script will take in to account the delay it takes for the Analytics tracking beacon to be sent, as well as different ways the user might interact with the link including using a modifier key to open the link in a new tab. 

You should already have Google Analytics installed and running on your website; this script will do nothing if Google Analytics is not found on your website. 

# How to use

1. Make sure you have jQuery included on your page. 
2. Embed link-click-analytics.js on your page. 
3. Add the attribute **data-analytics-event** to an HTML link or button on your web page.

Parameters are comma separated and correspond to the four parameters for Event Tracking: Category, Action, Label, and Value. So for example, you might add a parameter to your link that looks like this: 

```html
<a href="#" data-analytics-event="Big Red Button,Request Information,Page Footer">Click here</a>
```

If parameters are not specificed, they will default to the following values:

- Category: "Call to Action Link"
- Action: The inner text of the link
- Label: The URL (href attribute if present)
- Value: undefined


# Example

```html
<head>
	<script src="//ajax.googleapis.com/ajax/libs/jquery/2.1.0/jquery.min.js" type="text/javascript"></script>
	<script src="link-click-analytics.js" type="text/javascript"></script>
</head>
<body>
	<a href="http://www.google.com" data-analytics-event="MyCategory,MyAction,MyLabel,10">Buy my product!</a>
</body>
```

# Notes

The script will allow users to use the modifier keys like Control and Command to open links in new tabs, and will still track clicks. 
