# Django views
## What is a View?
A view function, or view for short, is a Python function that takes a Web request and returns a Web response. This response can be the HTML contents of a Web page, or a redirect, or a 404 error, or an XML document, or an image . . . or anything, really. The view itself contains whatever arbitrary logic is necessary to return that response. This code can live anywhere you want, as long as it’s on your Python path. There’s no other requirement–no “magic,” so to speak. For the sake of putting the code somewhere, the convention is to put views in a file called views.py, placed in your project or application directory.

## How Django processes a request
When a user requests a page from your Django-powered site, this is the algorithm the system follows to determine which Python code to execute:

1. Django determines the root URLconf module to use. Ordinarily, this is the value of the ROOT_URLCONF setting, but if the incoming HttpRequest object has a urlconf attribute (set by middleware), its value will be used in place of the ROOT_URLCONF setting.
2. Django loads that Python module and looks for the variable urlpatterns. This should be a Python list, in the format returned by the function django.urls.patterns().
3. Django runs through each URL pattern, in order, and stops at the first one that matches the requested URL.

## How Django processes a response

1. Django determines the root URLconf module to use. Ordinarily, this is the value of the ROOT_URLCONF setting, but if the incoming HttpRequest object has a urlconf attribute (set by middleware), its value will be used in place of the ROOT_URLCONF setting.
2. Django loads that Python module and looks for the variable urlpatterns. This should be a Python list, in the format returned by the function django.urls.patterns().
3. Django runs through each URL pattern, in order, and stops at the first one that matches the requested URL.

### Things I want to know more about? More about Django views and how to use them.