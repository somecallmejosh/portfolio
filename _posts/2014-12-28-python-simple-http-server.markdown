---
title:  "Python Simple HTTP Server"
date:   2014-12-28 17:05:48
categories: python
main_image: "knight.jpg"
flickr_attribution: Andrew Becraft
flickr_link: https://www.flickr.com/photos/dunechaser/103312153/in/photolist-a8v72-pX2oF-4nbthP-7a2Up7-4XAGq3-9S9Rai-iG1qpv-S9LYs-4DMcmF-asWkQH-7DBGmA-9mLPZH-5r6oaB-dA7Sw8-5GGucN-5LXQkJ-purgS2-7f9dP6-w3gzq-no3t1m-jyBxzy-dfWvS3-5d1sVr-bAiZef-6MRqsg-6eG1mj-5EZRHb-5pU3oT-bygWSH-bVa71J-pJmaQG-6VEa4N-hcoPsn-bjukAY-6wi4y1-4xkD1r-bDpRan-5z4Nui-5nK5FY-4bn1Bv-9544tB-5qpSDx-9n2hWk-5aMBSw-o3u78f-955ydC-9aAUWt-6xhyge-8pgZEm-5qpSCZ
flickr_license: "https://creativecommons.org/licenses/by-nc-nd/2.0/"
---

When I’m building a simple project, I just want to get a simple server up and running with little to no fuss. I don’t use MAMP or WAMP or XAMP or any of those things because I rarely do anything that requires them (I’m not suggesting they’re bad). Since I’m on a Mac, and Python is already installed, I just use the SimpleHTTPServer.

In the terminal, navigate to the web project, and type the following:

`python -m SimpleHTTPServer 8000`

Then, head over to the browsers and type this into the address bar:

`http://localhost:8000`

Kaboom!
