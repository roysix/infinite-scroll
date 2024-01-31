# Infy Scroll
<img src="https://raw.githubusercontent.com/sixcious/assets/main/repository/infy-scroll/icon.svg?sanitize=true" width="196" height="196" alt="Infy Scroll" title="Infy Scroll">

## Available For
<a href="https://chrome.google.com/webstore/detail/infy-scroll/gdnpnkfophbmbpcjdlbiajpkgdndlino" title="Download for Google Chrome"><img src="https://raw.githubusercontent.com/sixcious/assets/main/vendor/chrome.svg?sanitize=true" height="64" alt="Google Chrome"></a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href="https://microsoftedge.microsoft.com/addons/detail/infy-scroll/fmdemgjiipojpgemeljnbaabjeinicba" title="Download for Microsoft Edge"><img src="https://raw.githubusercontent.com/sixcious/assets/main/vendor/edge.png" height="64" alt="Microsoft Edge, Icon: By Source, Fair use, https://en.wikipedia.org/w/index.php?curid=62848768"></a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href="https://addons.mozilla.org/firefox/addon/infy-scroll/" title="Download for Mozilla Firefox"><img src="https://raw.githubusercontent.com/sixcious/assets/main/vendor/firefox.svg?sanitize=true" height="64" alt="Mozilla Firefox"></a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

<br><br><br>
<img src="https://raw.githubusercontent.com/sixcious/assets/main/repository/infy-scroll/infy.png" height="600" alt="Infy" title="Infy" align="left">

## Important Note
Infy is currently in beta. This means it might contain a few bugs and it might not work on every website you try it on! But I really want you to be 100% happy with Infy, so if something isn't working right, or if there's a feature you think is missing, please open an issue on GitHub and give me a chance to fix it before leaving a low rating/review, and I promise I will.
<br><br>
### Discord
Join the new Discord! (Beta) 💜
<br><br>
<a href="https://discord.gg/Z63tmCx4q5" title="Join the Discord"><img src="https://raw.githubusercontent.com/sixcious/assets/main/vendor/discord.svg?sanitize=true" height="64" alt="Discord"></a>
<br><br><br><br><br><br><br><br><br><br><br>

## About
Infy Scroll can let you add customized infinite scrolling to websites and auto load the next page as you scroll down. It's also compatible with the AutoPagerize Database, which means it supports thousands of websites automatically. Infy supports 4 different actions and 6 different append modes so you can customize each site's infinite scrolling to how you want it to be. Infy understands both CSS Selector and XPath expressions for finding next links, and it features an Element Picker that can generate them for you, similar to the original AutoPager. It can also increment URLs and perform special actions, like clicking "Load More" buttons. You can save your settings for each URL and Infy will auto-activate the next time you visit them.

## Features
- 4 Actions: Next Link, Click Element, Increment URL, URL List
- 6 Append Modes: Page (for simple websites), Iframe (for complex websites), Element (AutoPagerize Mode), Media (for images like 001.jpg), AJAX (for AJAX/SPA sites), and None (for sites that only require clicks)
- Paths: Infy understands CSS Selectors, XPath expressions, and JS Paths, and can auto-detect what type of path you are entering, or can be set to a fixed path type by toggling the label (SE/XP/JS)
- Element Picker: Pick an element on the page and generate its Selector or XPath expression automatically or use the EP's buttons to traverse the DOM in any direction (May not work on complex websites)
- Auto Detect (an innovative feature): Let Infy's algorithm try to detect the next link, page element, and click elements for you (May not work well on complex websites)
- Auto Mode: Automatically append pages, or use Slideshow Mode (supports Pause and Repeat)
- AJAX Support: Infy features two unique AJAX append modes: Iframe and Native (Experimental)
- SPA Support: Infy supports the Navigation API to detect navigation events and can use a MutationObserver to watch for changes on the page to provide compatibility with many complex AJAX and Single-page Application sites (Experimental)
- Save URLs: Infy can save custom site-specific settings and then auto-activate on your favorite URLs
- Database Support: Infy supports the AutoPagerize and InfyScroll Databases allowing it to support thousands of websites for you automatically
- Custom Scripts: Infy has custom scripts for a few popular websites (such as Google Search) that will try to fix missing image thumbnails
- Advanced Features: Fix lazy loading or use the Element Iframe mode to fix missing images
- User Interface: A simple UI custom built using Material Design
- Mobile Support: Support for Firefox for Android and Kiwi Browser (Some features may not work perfectly)
- Uses 0 Background Memory when inactive
- No Ads, No Tracking, No Bloat

## Introducing AJAX
Since releasing Infy Scroll in August 2020, if you were to ask me what is the one feature I was working my hardest to implement — it's always been an append mode for [AJAX websites](https://developer.mozilla.org/docs/Glossary/AJAX). After two years of on and off development, I'm really proud to offer this [completely new and innovative append mode](https://github.com/sixcious/infy-scroll/wiki/AJAX) in Version 0.8, The Eightfinity Edition. AJAX comes in two versions: Iframe and Native. AJAX is mostly in the proof of concept stage right now, but does work on many sites, including Pixiv.

#### AJAX Demo (Pixiv)
<img src="https://raw.githubusercontent.com/sixcious/infy-scroll/main/assets/ajax.gif">

##### Settings Used:
````
{
  "action": "click",
  "append": "ajax",
  "clickElement": "//nav/button[@aria-current='true']/following-sibling::a[not(@hidden)]",
  "loadElement": "//section//div/ul//figure",
  "pageElement": "//section/div/ul | //section/div/div/ul | //section/div/div/div/ul",
  "spaf": "^https://www\\.pixiv\\.net",
  "url": "^https://www\\.pixiv\\.net/"
}
````
*You can copy and paste these settings using the Add Save feature in the Options. (Tested on December 22, 2022.)*

## SPA Support
[SPAs (Single-page Applications)](https://developer.mozilla.org/docs/Glossary/SPA) are tricky to deal with because they update their page content dynamically, and sometimes don't even update the address bar. However, Infy now supports the [Navigation API](https://developer.mozilla.org/docs/Web/API/Navigation_API) (Chrome/Edge 102+ Only) to detect browser navigations and it can also watch for changes on the page and auto-activate and auto-deactivate itself if the website changes its content dynamically. It even works here on GitHub and on Pixiv. (If you're on Firefox, you can check the Late Activation setting in the UI Window's Scripts dialog and save the URL.) No more refreshing the page!

## Installation
Installing from GitHub is super simple. First, [download the zip](https://github.com/sixcious/infy-scroll/archive/refs/heads/main.zip) and unzip it. Then:

#### Chrome and Edge
- [Follow these instructions](https://developer.chrome.com/docs/extensions/mv3/getstarted/development-basics/#load-unpacked) to enable Developer Mode and load an Unpacked Extension

#### Firefox
- [Follow these instructions](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension#installing) to load a Temporary Add-on

**Finally**: When prompted for the location, select the `src/base` folder (Firefox: select `manifest.json`) and it will install.

**Important**: There is no version update path for the GitHub build, so use the [web store version](https://github.com/sixcious/infy-scroll#available-for) as your main version.

## Help Guide
[View the Help Guide!](https://github.com/sixcious/infy-scroll/wiki)

## Documentation
- [Version History](https://github.com/sixcious/infy-scroll/wiki/Version-History)
- [Future Roadmap](https://github.com/sixcious/infy-scroll/wiki/Roadmap)

## FAQ

#### What happened to the Append Scripts and Styles options?
I'm real sorry, but due to the new Manifest V3 (MV3) restrictions, I was forced to remove these two settings starting in Version 0.8. Luckily, there's a great workaround: you can still append iframes, and iframes will always contain the scripts and styles for each page. Iframes are actually the better approach for this purpose as the scripts and styles will run in an isolated environment inside the iframe without affecting the top-level document. If a website is preventing you from appending iframes, please try using [Xframey](https://github.com/sixcious/xframey) or a similar app/extension. I'm very sorry once again.

#### What happend to the Custom Database and Save Whitelist?
I'm super sorry, but starting in Version 0.8, these two collections have been merged into your [Saves](https://github.com/sixcious/infy-scroll/wiki/Saves). The reason I had to merge them is because of how complex the activation code has become. As you can imagine, it became extremely hard to manage four different collections: Saves, Regular Database, Save Whitelist, and Custom Database. I decided to invest heavily into further developing Saves.

#### Can you help me make it work with a specific website?
I really wish I could! Please see the [Sticky Thread](https://github.com/sixcious/infy-scroll/issues/50) for a potential solution.

#### Why can't Infy Scroll execute custom scripts?
Unfortunately, because browsers strongly discourage this from a security standpoint (especially now that Manifest V3 is out!). However, there's a workaround: you can write your own custom scripts inside a Userscript Manager (like [Violentmonkey](https://github.com/violentmonkey/violentmonkey)) by listening for Custom Events that Infy triggers whenever a new node or page has been appended or by implementing a [MutationObserver](https://developer.mozilla.org/docs/Web/API/MutationObserver). Feel free to read the [Scripts and Styles](https://github.com/sixcious/infy-scroll/wiki/Scripts-and-Styles) section for examples and more information.

#### What is the minimum browser version (and why is it to so high)?
Infy currently requires Chrome/Edge/Firefox `102` and higher to run. I tend to update the minimum browser version about once a year so I can use the latest and greatest ECMAScript features without worry. It also significantly saves in my testing time in having to maintain older Chromium builds. In the past, I used to offer "modified" builds with a lower minimum version, but I can no longer do this. If your browser doesn't support Infy, I'm afraid you'll have to use another app/extension (sorry!).

#### Why is the production version's source code minified?
I use [Terser](https://github.com/terser/terser) to minify the source code for production releases that I upload to your browser's web store. I mainly do this because I write a lot of comments and `console.log()` statements for debugging that you don't want to have and because it cuts down the file size significantly. That said, you can always view a "Pretty Print" of the source code by using a [CRX Viewer](https://robwu.nl/crxviewer/) to inspect it before installing it.

## Permissions Justification
- `Read and change all your data on the websites you visit` - Infy needs to request this permission so that its content script can auto-activate on any Saved URL or Database URL you want it to.

## Privacy Policy
Infy Scroll does *not* track you. It does *not* use analytic services. It does *not* collect or transmit any data from your device or computer. All your data is stored locally on your device. Your data is *your* data.

## Credits and Special Thanks
<ul>
  <li>Infy: <a href="https://twitter.com/thejoyfool" target="_blank">Joyfool</a></li>
  <li>UI: <a href="https://material.io" target="_blank">Material Design</a></li>
  <li>Fonts: <a href="https://fonts.google.com/specimen/Roboto" target="_blank">Roboto</a>, <a href="https://fonts.adobe.com/fonts/lithos" target="_blank">Lithos</a></li>
  <li>Icons: <a href="https://fontawesome.com" target="_blank">FontAwesome</a>, <a href="https://github.com/feathericons/feather" target="_blank">Feather</a></li>
  <li>Animations: <a href="https://ianlunn.github.io/Hover" target="_blank">Hover.css</a></li>
  <li>Tooltips: <a href="https://kazzkiq.github.io/balloon.css" target="_blank">Balloon.css</a></li>
  <li>Loading: <a href="https://loading.io" target="_blank">Loading.io</a></li>
  <li>Charts: <a href="https://github.com/chartjs/Chart.js" target="_blank">Chart.js</a></li>
  <li>Confetti: <a href="https://github.com/catdad/canvas-confetti" target="_blank">Canvas Confetti</a></li>
  <li>Resizing: <a href="https://github.com/davidjbradshaw/iframe-resizer" target="_blank">Iframe Resizer</a></li>
  <li>Hover Box: <a href="https://github.com/AlienKevin" target="_blank">AlienKevin</a></li>
  <li>DOM Paths: <a href="https://github.com/chromium/chromium" target="_blank">Chromium</a></li>
  <li>CDNs: <a href="https://www.jsdelivr.com" target="_blank">Jsdelivr</a>, <a href="http://statically.io" target="_blank">Statically</a></li>
  <li>Database: <a href="http://wedata.net/users" target="_blank">Wedata Contributors</a></li>
  <li>Shoutout To: <a href="#AutoPagerByWindLi">AutoPager</a>, <a href="https://github.com/swdyh/autopagerize" target="_blank">AutoPagerize</a>, <a href="https://github.com/hoothin/UserScripts/tree/master/Pagetual" target="_blank">Pagetual</a>, <a href="https://github.com/jkoomjian/PageZipper" target="_blank">PageZipper</a>, <a href="https://github.com/machsix/Super-preloader" target="_blank">Super-preloader</a>, <a href="https://github.com/Griever/userChromeJS/tree/master/uAutoPagerize">uAutoPagerize</a></li>
  <li>With Special Thanks: <a href="#lostpacket">LostPacket</a>, <a href="#daydreaming5">DayDreaming</a>, <a href="https://github.com/Tanookirby" target="_b
  '}:lank">Tanookirby</a>, and <a href="https://github.com/alexolog" target="_blank">Alex</a></li>
</ul>

... and most of all you for using Infy

## Contributing
Thanks for considering to contribute! I'm currently not setup to accept PRs just yet, but you can [open an issue](https://github.com/sixcious/infy-scroll/issues) and we can discuss your idea or change.

## License
<a href="https://github.com/sixcious/infy-scroll/blob/main/LICENSE">View License</a>  

## Copyright
Infy Scroll  
Copyright &copy; 2015-2020 <a href="https://github.com/sixcious" target="_blank">Roy Six</a>  
Character Design and Artwork Copyright &copy; 2020 <a href="https://twitter.com/thejoyfool" target="_blank">Joyfool</a>
