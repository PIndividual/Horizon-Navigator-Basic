# Horizon Navigator


***Please be advised that as I'm introducing the capital city of China, the hyperlinks on this microsite will most likely be directed to a Mandarin page, use web translators if possible :)***

## Implementation decisions

This microsite is designed to serve as a simple guide for people travelling to Beijing for the first time, and it aims to provide a place where people can quickly learn about famous local attractions and customs as well as special events.

My microsite features several benefits:

* Major attractions, events and festivals are all gathered on this microsite, so no more massive Google search for a proper travel guide that fits your timing.
* Users can quickly find what they need on the microsite and can always access the source through the hyperlink.
* The site serves only as a simple navigator and takes information from the source, the content is always up-to-date, so not misleading and outdated info.

My design is based on Beijing, China's capital and political centre. This is a city full of history with many places of interest. There are 3 main functions on my microsite:

1. The home page introduces the city with a few recommendations to get you quickly started.
2. The discover page lists the famous attractions, by toggling the display filter, you can also see some famous festivals.
3. The timeline page displays recent events, you can use a time slider to look at upcoming or past events within the current year.

## Mockups and prototype comparisons

![Home page](image/readme/1699589088486.png "Left: prototype Right: mockup")

I found that using gradient masking to fit the image into the right side of the text is a hard approach without the help of javascript, so I ended up using separate divs to fill in the image and the text, under the container div (coloured yellow as background).

To enhance the sense of hierarchy and to add a bit more detail, I put rounded corners on the image and added some shadows.

![Navbar & colour](image/readme/1699590091984.png "Left: prototype Right: mockup")

I replaced the dark context colour from black to dark red so it creates a better consistency with other colours and still maintains a good contrast.

The navbar now has a simplified look on narrow browser windows in order to improve the experience for mobile users. The logo now hides when clicking on it as it does no difference with the "Home" tag. The links now expand to evenly split the horizontal space of the browser window, making it easier to select.

## Further iterations/improvements

Currently, the microsite has a complete shape but seems a bit stiff, most elements on the page are static. I plan to add more user interaction feedback on the microsite.

For example, when the mouse hovers over an image, the image becomes bigger and slightly 3D rotates according to the mouse position, feels like it's popping out from the microsite. Things like this will significantly boost the user experience.

## Iconic code blocks

```html
<div class="video-container">
    <!-- From https://www.w3schools.com/tags/tag_video.asp-->
    <video autoplay loop muted >
      <source src="vid.mp4" type="video/mp4">
    </video>
    <!-- To make sure the texts are sharp and sticks to the same position on the video the all time, I set up a new div for them -->
    <!-- These are essentially h1 and h2, but I used a specific name for them so it is easier to locate them in css-->
    <vidTitle>Welcome to Horizon Navigator</vidTitle>
    <vidSub>Discover, familiarise and explore</vidSub>
  </div>
```

```css
.video-container vidTitle {
  position: absolute; /* The anchor position of the text is modified here (for the entire video) */
  top: 50%;
  left: 50%;
  transform: translate(-50%, -100%); /* The text position is slightly tuned for the new anchor position */
  font-family: TSYT;
  color: white;
  white-space: nowrap;/*The texts are not supposed to auto wrap*/
  font-size: 5vw;/*When the window width changes, the text size changes as well*/
}

.video-container vidSub {
  position: absolute; /* Same as the VidTitle */
  top: 50%;
  left: 50%;
  transform: translate(-50%); 
  font-family: HarmonyOS;
  color: white;
  font-size: 3vw;
  /*box-shadow: 0 3px 6px rgba(0, 0, 0, 0.2); I was planning to add shadows to the texts on the video as well, but they ended up making a transparent border with shadows, so I have to disable this line*/
}

```

This is the part where I created multiple divs to fit in the video and the texts above it.

There are also codes coming from external referencing documents such as the code that **stops the rubberband effect**.

```css
overscroll-behavior: none; /*This will prevent the browser's built-in rubber band effect when scrolling, from https://developer.mozilla.org/en-US/docs/Web/CSS/overscroll-behavior */
```

And this line adds **colour and corner radius transition**.

```css
transition: background-color 0.3s ease, border-radius 0.3s ease;/*https://stackoverflow.com/questions/7048313/how-to-have-multiple-css-transitions-on-an-element*/
```

## References

* Afif, T. (2023, May 18).  *How to Create a Custom Range Slider Using CSS — SitePoint* . Www.sitepoint.com. https://www.sitepoint.com/css-custom-range-slider/
* Beijing Water Authority. (2022, January 17).  *八一湖开启冰上嘉年华_工作动态_北京市水务局* . Swj.beijing.gov.cn. https://swj.beijing.gov.cn/swdt/swyw/202201/t20220117_2593271.html

* emmby, hey. (2023, May 11).  *A tall building with a bird flying over it* . Unsplash.com. https://unsplash.com/photos/a-tall-building-with-a-bird-flying-over-it-yfco6U3snKo
* 风嘲. (2019, March 19).  *Brown roof* . Unsplash.com. https://unsplash.com/photos/djcZLQrzL2Y

* Ge, Y. (2020).  *从《吐槽大会》到《笑场》，脱口秀节目搅动喜剧演出市场* . Yicai.com. https://m.yicai.com/news/100551923.html
* kaiyv, zhang. (2018, September 20).  *black high rise builcing* . Unsplash.com. https://unsplash.com/photos/9v_Nork6P1w

* kaiyv, zhang. (2020, September 8).  *Brown and green building near body of water under blue sky during daytime* . Unsplash.com. https://unsplash.com/photos/alGTmO0KvJI
* kaiyv, zhang. (2021, February 23).  *People walking on street near high rise buildings during night time* . Unsplash.com. https://unsplash.com/photos/vgLNs0TmeCY

* Lu, H. (2017, October 24).  *Great Wall Of China, China* . Unsplash.com. https://unsplash.com/photos/_8EFj6ISA08
* 卖橘子的heixin老板. (2017, April 9).  *北京图片城市剪影_民俗人文_生活方式-图行天下素材网* . Www.photophoto.cn. https://www.photophoto.cn/pic/23713936.html

* Microsoft. (n.d.).  *Image Creator from Microsoft Bing* . Bing. https://www.bing.com/create
* Mozilla. (n.d.-a).  *transition - CSS: Cascading Style Sheets | MDN* . Developer.mozilla.org. https://developer.mozilla.org/en-US/docs/Web/CSS/transition

* Mozilla. (n.d.-b).  *Using CSS transitions - CSS: Cascading Style Sheets | MDN* . Developer.mozilla.org. https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions
* Mozilla. (2023a, February 22).  *::-webkit-slider-thumb - CSS: Cascading Style Sheets | MDN* . Developer.mozilla.org. https://developer.mozilla.org/en-US/docs/Web/CSS/::-webkit-slider-thumb

* Mozilla. (2023b, October 6).  *overscroll-behavior - CSS: Cascading Style Sheets | MDN* . Developer.mozilla.org. https://developer.mozilla.org/en-US/docs/Web/CSS/overscroll-behavior
* Mozilla. (2023c, October 14).  *: The Anchor element - HTML: HyperText Markup Language | MDN* . Developer.mozilla.org. https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a#attr-href

* Thoma, E., & Köberle, A. (2011, July 1). *How to have multiple CSS transitions on an element?* Stack Overflow. https://stackoverflow.com/questions/7048313/how-to-have-multiple-css-transitions-on-an-element
* TOPYS. (2020, June 18).  *航拍北京｜TOPYS* . Www.youtube.com. https://www.youtube.com/watch?v=rbxBWDnQIZw

* W3schools. (n.d.-a).  *HTML a target Attribute* . Www.w3schools.com. https://www.w3schools.com/tags/att_a_target.asp
* W3schools. (n.d.-b).  *HTML video Tag* . Www.w3schools.com. https://www.w3schools.com/tags/tag_video.asp

* Wandering Shadow Seeker. (2011, November 15).  *The Summer Palace Through My Lens* . Wandering Shadow Seeker. https://wanderingshadowseeker.wordpress.com/2011/11/15/the-summer-palace-through-my-lens/
* Wikipedia Contributors. (2018, December 11).  *Great Wall of China* . Wikipedia; Wikimedia Foundation. https://en.wikipedia.org/wiki/Great_Wall_of_China

* Wikipedia Contributors. (2019, May 9).  *Beijing* . Wikipedia; Wikimedia Foundation. https://en.wikipedia.org/wiki/Beijing
