# McDonald's Homepage Clone

A recreation of the McDonald's homepage using only HTML and CSS. I focused on general layout more than pixel perfection.

# What I learned

I learned that responsive flexbox behavior can be affected by other elements that can't be shrunk further such as fixed-images on the screen.

I learned that `overflow: hidden` applies to direct children only.

Learned to deploy my project in a live server for real-time updating while debugging.

Learned that it's good practice to have a catchall `container` class to center objects on the page.

# Challenges

While trying to make the website responsive, I came across a time consuming interaction where the width of my header would shrink faster than the viewport shrank.

After some debugging, I realized this behavior occurred right around the point when the viewport width became smaller than some fixed-width images on the page.

When an image has a fixed width and the viewport becomes smaller than that, the browser tries to preserve the image’s size instead of scaling it down. This causes the body to overflow horizontally, effectively widening the layout beyond the viewport.

Thus, percentage based elements are calculated based on this adjusted layout width, not the actual visible screen.
