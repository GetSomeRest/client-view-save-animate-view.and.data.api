
#client sample - ViewSaveAnimate

The MIT License (MIT)

Copyright (c) 2014 Autodesk, Inc.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

##Description

*This sample is part of the [Developer-Autodesk/Autodesk-View-and-Data-API-Samples](https://github.com/Developer-Autodesk/autodesk-view-and-data-api-samples) repository.*

This sample shows how you can save/restore views in the viewer and the play them in a loop in order to animate going from one saved view to the next. The webpage is using a jQuery UI sortable component to store the views the user saves.
It enables you to 
- drag&drop sort the saved view buttons
- drag buttons off the toolbar to remove them
- switch to any saved view
- animate the saved views

Buttons:
- "S": saves the current view. You can also use Alt+S to do the same
- "A": animates the stored views. It will start on the first view in the toolbar and keep switching to the next stored view until the last one is reached.
- "1".."n": the stored views

##Dependencies

You need other workflow samples to log in, upload a file, start translation to get required parameters.

##Setup/Usage Instructions

It requires the user to pass in a valid access token and urn of the file they want to use as a URL parameter:
- ViewSaveAnimate.html?accessToken=&lt;access token&gt;&urn=&lt;urn of the file to view&gt;
- e.g.: ViewSaveAnimate.html?accessToken=ljvWwXkzF3zxCVfLUZhP1Q8Qk66S&urn=dXJuOmFkc2sub2JqZWN0czpvcy5vYmplY3Q6bXl0ZXN0YnVja2V0L2NoYXNzaXMuZHdm

You can use e.g. the https://github.com/Developer-Autodesk/workflow-wpf-view.and.data.api sample to log in, upload a file, start translation and then invoke this html page with the required parameters. 

The html page has two parameters you can adjust:
- MyClass.kInBetweenSteps: this sets how many extra steps are added in between the stored views when animating, to make it smoother
- MyClass.kMilliSecondsBetweenSteps: the time in milliseconds that we'll wait before switching from one saved view to the next when animating


##Written by 

Adam Nagy








