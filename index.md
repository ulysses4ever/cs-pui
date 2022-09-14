---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home

header: 
    overlay_image: img/teach-research.png

---
<link rel="stylesheet" href="cspui.css">

![continuum of teaching and research](img/cs-pui-listing.jpg)


📣 **If you would like to add your position,** [please visit the **Post an Ad** page](/posting) for logistical details or the [**FAQ**](/faq) for more info about this site (it's free!). 
{: .notice .notice-blue}

In 2017, I [wrote an article about finding academic happiness with **primarily-undergraduate institutions**](https://medium.com/bucknell-hci/the-jobs-i-didnt-see-my-misconceptions-of-the-academic-job-market-9cb98b057422) because of the compelling balance they offer between teaching and research. I continue to receive emails with the same  question: _how do I find these jobs?_ This listing of ads is meant to help navigate that muddy water. [See archived listings from previous years](faq#archive).

This document does _not_ contain most CS faculty positions. It's specifically intended for people who want to invest in teaching/mentorship with undergraduate students while still staying active in their scholarship. 

{% capture criteria %}
**Criteria:** the positions on this page should be...
- accessible to those with a Ph.D. in CS (or a closely related field)
- permanent positions (mostly likely tenure-track) [_why?_](faq#scope)
- universities that identify as **primarily-undergraduate institutions** [_why?_](faq#scope)
- institutions that highly value teaching, but also _secure time and financial resources for faculty to remain engaged with research_. [_what does this mean?_](faq#research)
{% endcapture %}
<div class="notice notice-gray">{{ criteria | markdownify }}</div>
{: #criteria}

If you are considering entering the job market, I'd encourage you to visit the [**Resources**](resources.html) pages for some insight into the ways in which PUIs might differ in their interviewing processes and values.

------------

# Who is hiring in CS so far (2022/23)


## 📋 Deadlines and Quick Links (_soonest on top_)
{: #deadlines}

💡 **Deadlines are treated very differently between institutions**. Read carefully. For example, I _strongly_ encourage you to email search chairs if you're interested in positions that appear to have passed - they might still be open!
{: .notice .notice-blue}

{% assign deadline_sorted_posts = site.posts | sort: 'deadline' | reverse %}
<div class="styled-table">
  <table>
  <thead>
    <tr>
      <th style="text-align: left"><strong>Institution</strong></th>
      <th style="text-align: left"><strong>Location</strong></th>
      <th style="text-align: left"><strong>App Deadline</strong></th>
    </tr>
  </thead>
  <tbody>
    {% for post in deadline_sorted_posts %}
    <tr>
      <td style="text-align: left"><a href="#{{ post.tag }}">{{ post.title }}</a></td>
      <td style="text-align: left">{{ post.location }}</td>
      <td style="text-align: left">{{ post.deadline | date: "%m/%d/%Y" }}</td>
    </tr>
    {% endfor %}
  </tbody>
  </table>
</div>


------------

## 📣  Ads, Links, and Locations (_alphabetical order_) 

{% assign alpha_sorted_posts = site.posts | sort: 'institution' | reverse %}
<div class="jobs">
{% for post in alpha_sorted_posts %}
  <h3 id="{{ post.tag }}">{{ post.title }}</h3>
  {{ post.description | markdownify }}
  <p><a href="{{ post.link }}" class="button-job">Full Job Posting</a>
  <a href="#deadlines"><em>back to all deadlines</em></a></p>
{% endfor %}
</div>
