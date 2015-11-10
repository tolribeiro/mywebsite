---
layout: post
title:  "My very fist iOS App: controlling work hours"
description: "A very simple app to help couting hours at work"
date:   2015-10-27 21:53:05
categories: jekyll update
---
n the month of May, this year, I decided to dive into the world of mobile development. For that reason, 
I accepted the challenge of joining a company specialized of that field, where I would learn, practice daily, and also, get  myself very immersed in the culture of developing applications that run in smartphones, specially iPhones.

Therefore, in the very first days of my internship, I was told that I should fill out a spreadsheet (on paper, it couldn't be digital) stating the arrival time, if I had stopped to eat during the day, and the time I was leaving the company.  

Even though I had heard that there was a spreadsheet set up that could do the job, I saw in that an opportunity to develop my skills in iOS as I started to create an app to do all the math for me. Then I would only have to write the times down on paper at the end of my workday. 

<div style="text-align:center" markdown="1">
![Message Signal](http://tolribeiro.github.io/mywebsite/downloads/minhasHorasNoData.jpg "First screen, to fill out with the times.")
</div>

In the empty forms, I manually enter the times (24-hour style in Brazil) during the day and press calculate to see how many hours I had worked until the break, the duration of my break, after and in total, as you can see below:

<div style="text-align:center" markdown="1">
![Message Signal](http://tolribeiro.github.io/mywebsite/downloads/minhasHorasData.jpg "App showing the elapsed time calculated.")
</div>

As I kept researching about how to calculate elapsed time, I got to know about NSDate and NSTimeInterval, which I believe is a more appropriate way to implement such apps. Nonetheless, at the time, I designed the algorithm "by hand", by getting the interval between the integers and returning the elapsed time. Thus, in Objective-C, I had:



{% highlight objective-c %}
-(void)calculaHorasGeral:(NSInteger)horaInicio:(NSInteger)minutoInicio:(NSInteger)horaFim:(NSInteger)minutoFim {
    
    NSInteger count = 0, total = 0, contador = 0;
    
    if (horaInicio < horaFim) {
        count = 60 - minutoInicio;
        horaInicio++;
        while (horaInicio < horaFim) {
            contador++;
            horaInicio++;
        }
        count = count + (contador * 60);
        total = count + minutoFim;
        horasTrabalhadasInt = total/60;
        minutosTrabalhadosInt = total % 60;
    } else if (horaInicio == horaFim) {
        if (minutoFim > minutoInicio)
            minutosTrabalhadosInt = minutoFim - minutoInicio;
    }
}
{% endhighlight %}

After a couple of months, I imagined a lot of other features that I could implement to make my app much more robust, such as storing the data, enabling the user to use the current time from the phone to mark the time, and so on.

Despite that, the experience of starting something on my own for iOS as a first application, even with such simple functionality, was very encouraging and kept me excited about the world of mobile development.
