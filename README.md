CSS is not a programming language, but it provides powerful functional tools and rule structures to make your styles more responsive, reusable, and maintainable.

# In this section, you’ll learn about:

> CSS Functions: calc(), var(), url(), min(), max()

> @-Rules: @media, @import, @font-face, @keyframes

> Real-world examples and use cases

# 1. CSS Functions Overview

calc() – Perform math in CSS

Use to calculate sizes dynamically:

      .container {
         width: calc(100% - 40px);
         padding: calc(1rem + 10px);
      }
      
 Useful for fluid layouts and spacing adjustments.

 # min() / max() / clamp()
These functions create responsive values without media queries.

        h1 {
            font-size: min(5vw, 32px); /* Use smaller of 5% viewport or 32px */
        }
       .card {
             width: clamp(300px, 50%, 600px); /* min, preferred, max */
       }
       
 clamp() is perfect for responsive typography and containers.

 # var() – CSS Variables
Define and reuse values:

          :root {
             --primary-color: #1e90ff;
             --padding: 1rem;
         }

      .button {
          background-color: var(--primary-color);
         padding: var(--padding);
     }
     
 Promotes consistency and easy theme updates.

 # url() – Link to resources (images/fonts)
 
       body {
            background-image: url("images/bg.jpg");
       }

# 2. CSS @-Rules (At-Rules):-

@media – Responsive Design
Apply styles conditionally based on screen size or device type.

    @media (max-width: 768px) {
        body {
             font-size: 14px;
         }

     .nav {
         flex-direction: column;
      }
   }
   
Common Breakpoints	       Device Type

> max-width: 768px	        Tablets/Phones

> max-width: 480px         	Mobile Phones

> min-width: 1024px        	Desktops/Laptops

 Essential for responsive design.

 # @import – Include External CSS Files
 
@import url('styles/colors.css');

 Not recommended over <link> in production (less performant).

# @font-face – Load Custom Fonts

         @font-face {
               font-family: 'MyFont';
               src: url('fonts/myfont.woff2') format('woff2');
        }
  
          body {
             font-family: 'MyFont', sans-serif;
          }
          
 Used when not relying on Google Fonts or want self-hosted fonts.

 # @keyframes – Create Animations
 
           @keyframes fade-in {
               from {
                  opacity: 0;
               }
               to {
               opacity: 1;
              }
          }

          .fade {
              animation: fade-in 1s ease-in-out;
          }
          
 Used with animation-name, animation-duration, etc.

 # Summary
Feature                             	    Example	                                                 Use Case

> calc();	                               width: calc(100% - 50px);	                      Dynamic sizes based on other values

> var();                                  color: var(--primary);                       	Reusable variables

> min()/max();	                           font-size: min(4vw, 32px);                  	Responsive design without media query

> @media;	                                @media (max-width: 768px);                 	Responsive layouts and breakpoints

> @import;	                                @import url('theme.css');              	     Modular CSS (limited use)
 
> @font-face;	                            Custom font loading;	                         Self-hosted font integration

> @keyframes;	                               CSS animations;	                            Transitions and UI feedback







