# How to use

1. Make sure you have jQuery included on your page. 
2. Embed link-click-analytics.js on your page. 
3. Add the attribute **data-analytics-event** to an HTML link on your web page.

Parameters are comma separated and correspond to the four parameters for Event Tracking: Category, Action, Label, and Value. So for example, you might add a parameter to your link that looks like this: **data-analytics-event="Big Red Button,Request Information,Page Footer"**

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

# Google Analytics Version

This script currently requires you to use the ga.js script which uses the global _gaq variable. 

https://developers.google.com/analytics/devguides/collection/gajs/eventTrackerGuide

# Notes

The script will allow users to use the modifier keys like Control and Command to open links in new tabs, and will still track clicks. 