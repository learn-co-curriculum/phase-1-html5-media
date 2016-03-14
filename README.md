# HTML5 Media

## Overview

In this lesson we will look at embedding audio and video into your HTML pages.

## Objectives

1. Embedding audio elements.
2. Embedding video elements.

## Audio and Video Elements

<iframe width="640" height="480" src="//www.youtube.com/embed/Jhz5qVW_1wo?rel=0" frameborder="0" allowfullscreen></iframe>

*Note: Slides for this lecture video are provided in the resources at the bottom of this lesson.*

### Audio

A nice feature of HTML5 is the ability to embed audio clips. We can do this by including the `<audio>` element. Enclosed within the audio element are `source` elements that point to the location of various audio file formats. The reason we provide multiple source files, is that not all browsers support both audio codecs required for playback. By providing both an MP3 as well as a OGG file we insure that all browsers will be able to play the content.

```html
<audio controls>
  <source src="purrr.mp3" type="audio/mp3">
  <source src="purrr.ogg" type="audio/ogg">
  <p>Sorry your browser doesn't support HTML5 Audio! Please <a href="http://browsehappy.com/?locale=en">upgrade your browser</a>.</p>
</audio>
```

<audio controls>
  <source src="http://ironboard-curriculum-content.s3.amazonaws.com/front-end/lab-assets/purrr.mp3" type="audio/mp3">
  <source src="http://ironboard-curriculum-content.s3.amazonaws.com/front-end/lab-assets/purrr.ogg" type="audio/ogg">
</audio>

On line 1 we start our opening `<audio>` tag. We have also inserted the `controls` attribute which is required to display the audio controls to start playback, pause, the recording etc. Notice that this particular attribute does not require a value. Just the presence of the attribute name itself is sufficent. There are additional attributes you can provide such as `autoplay` and `loop`. For the full list of accepted attributes check out the links below at the bottom of this lesson, for the MDN documentation. On lines 2 and 3 we provide two different source files for playback. If the browser does not recognize the first filetype it will ignore it and move on to the next. If neither of the formats are supported it will display the paragraph instead on line 4. If the browser is able to play one of the source files it will ignore any other code below until it reaches the closing `</audio>` tag. For source we must set the `src` location of the file by providing the relative path to the file, and the `type` which clues the browser as to which audio codec is suitable for that particular filetype.

### Video

We can also embed video clips into our pages. We do this by including the `<video>` element. Enclosed within the video element are `source` elements that point to the location of various audio file formats. The reason we provide multiple source files, is that not all browsers support both video codecs required for playback. By providing either an MP4 (h264) and OGV, or MP4 (h264) and WEBM file, we insure that all browsers will be able to play the content.

```html
<video controls>
  <source src="real-estate.mp4" type="video/mp4">
  <source src="real-estate.ogv" type="video/ogg">
  <p>Sorry your browser doesn't support HTML5 Video! Please <a href="http://browsehappy.com/?locale=en">upgrade your browser</a>.</p>
</video>
```

<video controls>
  <source src="http://ironboard-curriculum-content.s3.amazonaws.com/front-end/lab-assets/real-estate.mp4" type="video/mp4">
  <source src="http://ironboard-curriculum-content.s3.amazonaws.com/front-end/lab-assets/real-estate.ogv" type="video/ogg">
</video>

On line 1 we start our opening `<video>` tag with the `controls` attribute. For the full list of accepted attributes check out the links below at the bottom of this lesson. On lines 2 and 3 we provide two different source files for playback. If the browser does not recognize the first filetype it will ignore it and move on to the next just the same as it does for the audio element. If neither of the formats are supported it will display the paragraph instead on line 4. If the browser is able to play one of the source files it will ignore any other code below until it reaches the closing `</video>` tag. For source we must set the `src` location of the file by providing the relative path to the file, and the `type` which clues the browser as to which video codec is suitable.

### File Conversion

See the resource links at the bottom of the lesson for a few reccomended free audio and video converters you can use to change one file type to another. This is helpful to create both source file types needed. 

## Summary

- We can easily embed audio and video into HTML pages using the appropriate `<audio>` or `<video>` element.
- Media elements contain `<source>` elements within them that point to different source files. This insures the browser can play one or the other source type. Unsupported sources will be ignored and once a source file is usable all other code within the media elements block will be ignore.

## Resources

- [Presentation Slides](https://docs.google.com/presentation/d/1R2usO7eha-xvU6McOYjR8n2papGK-gzW_LwO4AM5NTA/edit?usp=sharing)
- [Audacity - Free Audio Editor/Converter](https://sourceforge.net/projects/audacity/)
- [MediaHuman - Free Audio Converter](http://www.mediahuman.com/audio-converter/)
- [Miro - Free Video Converter](http://www.mirovideoconverter.com/)
- [JavaScript HTML5 Video Player Comparison](https://praegnanz.de/html5video/)

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/HTML5-Media' title='HTML5 Media'>HTML5 Media</a> on Learn.co and start learning to code for free.</p>