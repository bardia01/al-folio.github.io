---
layout: page
title: ProPutter
description: an affordable golf trainer for beginners! 
img: /assets/img/proputter_background.jpg
importance: 2
category: work
---

<a href="https://github.com/itmr1/ProPutter">Repository link</a>.


<a href="https://bkmzad.wixsite.com/proputter">Concept website</a> 

ProPutter is an embedded systems project that attempts to improve the way beginners learn and improve their golf putting skills. Designed as a smart golf club, ProPutter leverages sensor technology and signal processing techniques to provide valuable insights and feedback to users about their performance while playing golf.

At the core of ProPutter lies an accelerometer which captures motion data during a golf putt. This raw data is then processed using filtering algorithms and other signal processing techniques to extract meaningful information about the user's putting technique.  

The processed data is wirelessly transmitted to a secure backend server, where it is intelligently analyzed and presented to the user through a sleek web application. The filtered putt is compared against reference data and a performance score based upon the deviation from the reference data is outputted. Ideally, we would have had a large dataset from professional golf putters which could be used to train a regression model about what a 'good putt' is, and hence the performance score would be generated from the model as opposed to the primitive algorithm we hand-made.

The web application serves as a comprehensive dashboard, providing users with a detailed overview of their putting performance, personalized recommendations for improvement, and the ability to compare their progress with friends.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/proputter_full.jpg" title="ProPutter" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The ProPutter prototype mounted onto a golf putter.
</div>


One of the notable technical successes of ProPutter is the implementation of advanced filtering algorithms. These algorithms effectively remove noise and artifacts from the accelerometer data, ensuring accurate and reliable measurements. Additionally, the integration of wireless communication protocols enables seamless data transfer between the golf club and the backend server, ensuring a seamless user experience.

ProPutter's intuitive web application showcases another technical triumph. Through a user-friendly interface, golfers can easily navigate and explore their performance metrics, track their progress over time, and access personalized tips to enhance their putting skills. The ability to compare their results with friends adds a competitive element, fostering a sense of community and motivation among users.

The integration of the temperature and humidity sensor adds another layer of insight to the ProPutter experience. By considering environmental factors, the system can provide golfers with a comprehensive understanding of how temperature and humidity may affect their putting abilities since they can track their performance across days with different environmental conditions.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/proputter_closeup.jpg" title="ProPutter" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The ProPutter prototype closeup. We can see the reset button, temperature and humidity sensor and the master reset button all mounted onto the battery pack.
</div>


ProPutter's success lies in the integration of different technical domains. The project showcases the effective collaboration of embedded systems, signal processing, wireless communication, and web application development. It demonstrates the potential of embedded systems to enhance traditional sports, while empowering beginners to take control of their golfing journey.


Overall, ProPutter stands as a testament to the power of integrating various technical disciplines to create a useful and accessible tool for golfers. Its aim is to assist beginners in improving their putting skills while embracing the potential of embedded systems in sports.