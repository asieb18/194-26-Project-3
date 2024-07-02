main.py
- This python file contains all of the methods and logic to run the project.
- It loads in two images to be morphed (im1 and im2), and gets and saves pairs of points (user-manually). If this step has already been done, it instead loads the saved files containing points.
- It computes the mid-way shape, then the entire sequence containing 46 frames starting from the original image 1 to the final second image.
- Next, it adds the reverse of sequence to make it a two way morph, then saves it as an animated gif.
- TO RUN THIS FILE, run main.py file in terminal. It will complete the steps described. Currently, it is set to run code to calculate the mean face of a population.
- Throughout the code comments, there are also sections to uncomment and allow the steps to be displayed along the process. In order to run the other functions, simply uncomment the corresponding lines at the bottom of the file (all labeled). 

- METHODS:
    - get_points(im1, im2, n): 
        - Prompts user to select n points on each image, and returns the list of points.
    - triangulation(pts, display): 
        - Given a set of points, returns Delaunay triangulation. Displays result if display=True.
    - computeAffine(tri1_pts, tri2_pts): 
        - Computes and returns affine warp matrix for given points
    - compute_midway(im1, im2, im1_pts, im2_pts):
        - Compute mid-way shape of images, returns average shape and blendded image.
    - warp(tri, im1, im1_pts, im2_pts):
        - Warps an image (im1) to the average shape (im2_pts), and returns resulting image.
    - def morph(im1, im2, im1_pts, im2_pts, warp_frac, dissolve_frac):
        - Produces a warp between two images using point correspondences and warp/dissolve frac
    - morph_sequence(im1, im2, im1_pts, im2_pts):
        - Creates a sequence of morphs with 45 frames.
        - Returns a list of images in sequence.
    - def mean_face(imgs, pts):
        - Returns a mean face given a list of imgs and corresponding points.
    - def caricature(im, im_pts, mean_pts, mean_img):
        - This returns and saves an image of a caricature created by extrapolating im from the mean_img. 


index.html / style.css
- This index file contains all of the code for the website. This includes all of the descriptions, images, and gifs. 
- The style.css file contains style formatting to oraganize the layout of the website, colors, and fonts used.
