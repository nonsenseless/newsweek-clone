Status (1/26/15): This project was completed as part of The Odin Project's Ruby on Rails course. The exercise requirements are listed [here](http://www.theodinproject.com/html5-and-css3/using-bootstrap) and the project successfully meets the requirements. The site displays properly at higher resolutions (992px+) but the alignment on some elements gets out of whack at lower resolution. 

Please note that I used Chrome's element inspector to copy font-family, font-size, letter-spacing, and color attributes as that seemed to be the better part of valor. 

# The Zen of Frameworks

I've used Bootstrap's grid and some JS features before, and I think I understood the components and how they functioned better now that I've spent more time on the individual HTML/CSS components and have a stronger mental model for how they go together, but there were still times where I felt like I was fighting with the framework to get things done. This was most prevalent when building the header and combining Bootstrap's suggested default header with the different elements used on Newsweek's header.

# Revision

## Class Names
An area I plan to address in revision is the proliferation of classes trying to identify the different sections of the page. I *believe* that Newsweek's Design Goal was to have a layout that let them present as much of the content of the magazine at one time as possible. Certainly, if there's any magazine content *not* linked on the main page, there can't be *much* of it. I added classes like 'teaser', 'cover-story', 'headline-stories', and 'other-stories' in order to try and capture the different areas of the page the stories were listed in and their distinct roles, but I feel like the result is a mess. Even as the one who wrote the files, I'd be hard-pressed to tell you the difference between 'headline-stories' and 'other-stories'. I suspect a simpler approach would be for each story card to have a single 'story' tag and the page division that contains it will have a section tag to distinguish it. For example,

.cover-teasers .teaser will become **.cover-teasers .story**, which will parallel **.headline-stories .story**

## Preprocessor
Per my personal preference, I'll update the project to use SASS, so that I can make better use of nesting, variables, and mixins.
