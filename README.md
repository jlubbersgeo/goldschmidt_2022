# Making a poster in `matplotlib`

On my most recent work trip, I had the idea to create a poster using 100% matplotlib. And once that idea entered my head it wouldn't leave. This was largely fueled by discussions on Illustrator vs. PowerPoint for creating conference posters I've seen on Twitter and I thought that neither were *technically* open-source. 

So I made my Goldschmidt 2022 poster using only matplotlib and importing one previously made diagram. Was this easier than illustrator? In some ways yes, in some ways no. Did I learn a lot doing it, definitely yes. Was it frustrating at times...also yes. Below are some tips on how to approach the task:

## Tips
1. read [this book](https://github.com/rougier/scientific-visualization-book) on scientific visualization using matplotlib by Nicolas Rougier. This has a lot of excellent visualization tips on how to maximize your information dissemination using matplotlib.
2. Matplotlib's `GridSpec` module is essentially the backbone of this entire project. It allows one to organize the figure into a grid of axis objects. The higher resolution the grid, the more freedom one has to make different size rectangles, but at the cost of keeping track of more axes. Ultimately this is where your discretion as a sceintist comes in!
    - This is an [excellent example](https://github.com/rougier/scientific-visualization-book/blob/master/code/layout/complex-layout-bare.py) on how to make a blank gridspec template. 
    - The layout for this poster is included as its own script in `poster_layout.ipynb`
3. Name axes based on their location in a predictable way. This will help you keep things organized. For example I did something like: `ax_umtr` which represents the **t**op **r**ight axis in the **u**pper **m**iddle section of the poster. 
4. Test all your figures and build them in a different cell/notebook. Many of the plots I included are actually initially generated in other notebooks/scripts first. When I have them the way I want them its as simple as copy and pasting the code for them into the notebook/script I'm using to make the poster. Makes the debugging and tweaking faster and less complicated.
5. Rather than adjusting the minutae of every plot, create an `rcParams` script that has this already established. I actually recommend doing this for much more than just posters if you like your plots to look a certain way, but in this case it helps you customize your figures without having to type the same thing over and over again
    - Here's an [example](https://github.com/rougier/scientific-visualization-book/blob/master/code/defaults/defaults-exercice-1.py)
6. Keep your text simple. This is probably a good rule of thumb for posters anyways, but I've found that paragraphs here don't work super well. Instead, bullet points are much more manageable in matplotlib and since there is `Tex` support you can use things like bullets, indents, math, etc. 
7. Have fun with it!
    - "Matplotlib makes easy things easy and hard things possible."

Happy poster making!

-- Jordan
