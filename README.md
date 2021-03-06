# RetinaDetection
A simulation of how the retina handles images and detects edges

We'll start by taking in an image. Let's try this robot:

  <img width="409" alt="screen shot 2018-06-04 at 12 25 19 pm" src="https://user-images.githubusercontent.com/30874015/40929911-243be01a-67f4-11e8-9782-00875033afb5.png">

  


First thing to do is form the retina filter. If you're familiar with convolutional neural nets, this is the same concept: running a filter over an image.

By the way, these axes are in pixels. I've included them so you can see the scale of the filter relative to the image. You'll notice the size of the filter is much smaller than the image, similar to how our eyes are smaller than many things we look at.

<img width="378" alt="screen shot 2018-06-04 at 12 25 30 pm" src="https://user-images.githubusercontent.com/30874015/40929531-07c5f25a-67f3-11e8-8e59-fd18099abf16.png">


Now that we have that, we just need to apply the filter. We'll use a difference of gaussians formula (a.k.a. the mexican hat formula), since at a basic level the retina captures light using this formula. It comes out looking like this:


<img width="382" alt="screen shot 2018-06-04 at 12 25 37 pm" src="https://user-images.githubusercontent.com/30874015/40929607-46f8a3dc-67f3-11e8-8de1-2a353ab4f0ef.png">


Now as you can see, the edges around the robot have become very clear to the program. The interior with many shadows and intricate parts is a little less clear to the program, just like it is a little less clear to a human what is going on there
