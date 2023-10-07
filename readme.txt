#Hello, Frontend Mentor community. This is my solution for the product preview card component challenge
This is challenge 2 where I provide comprehensive guidance to fellow developers by adhering to industry best practices. By focusing on key areas such as
•	Semantic HTML
•	Clean web page structure
•	CSS enhancements
•	Accessibility
•	Performance Optimization


I aim to address common mistakes observed in the challenges submitted by other participants. Through this initiative, I hope to not only solve newbie-level projects but also share valuable insights and tips to aid in their learning journey.

In this challenge I addressed common mistakes I found in others’ solutions 
1-	Displaying image
Most solutions handled this using Css display:none / display:block , instead you can use 
<picture> tag will look for the first <source> element where the media query matches the current viewport width, and display the proper image.
<img> element is required to be used as a fallback option if none of the source tags matches.

Note that you add class name and alt on the <img> not the <picture>

<picture>
    <source media="(max-width:650px)" srcset="./images/image-product-mobile.jpg"/>
    <source media="(min-width:650px)" srcset="./images/image-product-desktop.jpg"/>
    <img src="./images/image-product-desktop.jpg" alt="Gabrielle Chanel perfume" class="product__img"/>
  </picture>


2-	<del>
Adding a line through text with css 
This tag defines text that has been deleted from the document

3-	 Note that screen readers will read 2 prices right after each other , which will confuse the users , you can handle this by adding aria-label to both prices
```
   <ins class="price-current" aria-label="price after discount $149.99">$149.99 </ins> <del class="price-old" aria-label="price before discount $169.99"> $169.99</del>

```

If you have another way to make it accessible, kindly share it with us

This solution is tested by
•	lighthouse 
•	w3c validator
•	deque accessibility test
•	wave accessibility test
  
  

if you want me to review your code, just comment (the challenge name + the areas you want me to focus on) and I will provide a review as soon as possible.




