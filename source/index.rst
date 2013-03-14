Optimizing Software Occlusion Culling - index
#############################################
:date: 2013-02-17 15:33
:author: Fgiesen
:category: Coding

.. toctree::
   :maxdepth: 2
   :hidden:

In January of 2013, some nice folks at Intel released a `Software
Occlusion Culling demo`_ with full source code. I spent about two
weekends playing around with the code, and after realizing that it made
a great example for various things I'd been meaning to write about for a
long time, started churning out blog posts about it for the next few
weeks. This is the resulting series.

Here's the list of posts (the series is now finished):

#. `"Write combining is not your friend"`_, on typical write combining
   issues when writing graphics code.
#. `"A string processing rant"`_, a slightly over-the-top post that
   starts with some bad string processing habits and ends in a rant
   about what a complete minefield the standard C/C++ string processing
   functions and classes are whenever non-ASCII character sets are
   involved.
#. `"Cores don't like to share"`_, on some very common pitfalls when
   running multiple threads that share memory.
#. `"Fixing cache issues, the lazy way"`_. You could redesign your
   system to be more cache-friendly - but when you don't have the time
   or the energy, you could also just do this.
#. `"Frustum culling: turning the crank"`_ - on the other hand, if you
   do have the time and energy, might as well do it properly.
#. `"The barycentric conspiracy"`_ is a lead-in to some in-depth posts
   on the triangle rasterizer that's at the heart of Intel's demo. It's
   also a gripping tale of triangles, Möbius, and a plot centuries in
   the making.
#. `"Triangle rasterization in practice"`_ - how to build your own
   precise triangle rasterizer and *not* die trying.
#. `"Optimizing the basic rasterizer"`_, because this is real time, not
   amateur hour.
#. `"Depth buffers done quick, part 1"`_ - at last, looking at (and
   optimizing) the depth buffer rasterizer in Intel's example.
#. `"Depth buffers done quick, part 2"`_ - optimizing some more!
#. `"The care and feeding of worker threads, part 1"`_ - this project
   uses multi-threading; time to look into what these threads are
   actually doing.
#. `"The care and feeding of worker threads, part 2"`_ - more on
   scheduling.
#. `"Reshaping dataflows"`_ - using global knowledge to perform local
   code improvements.
#. `"Speculatively speaking"`_ - on store forwarding and speculative
   execution, using the triangle binner as an example.
#. `"Mopping up"`_ - a bunch of things that didn't fit anywhere else.
#. `"The Reckoning"`_ - in which a lesson is learned, but `the damage is
   irreversible`_.

All the code is available on `Github`_; there's various branches
corresponding to various (simultaneous) tracks of development, including
a lot of experiments that didn't pan out. The articles all reference the
`blog branch`_ which contains only the changes I talk about in the posts
- i.e. the stuff I judged to be actually useful.

Special thanks to Doug McNabb and Charu Chandrasekaran at Intel for
publishing the example with full source code and a permissive license,
and for saying "yes" when I asked them whether they were okay with me
writing about my findings in this way!

|CC0|

| 

To the extent possible under law,

Fabian Giesen

has waived all copyright and related or neighboring rights to

Optimizing Software Occlusion Culling.

.. _Software Occlusion Culling demo: http://software.intel.com/en-us/vcsource/samples/software-occlusion-culling
.. _"Write combining is not your friend": http://fgiesen.wordpress.com/2013/01/29/write-combining-is-not-your-friend/
.. _"A string processing rant": http://fgiesen.wordpress.com/2013/01/30/a-string-processing-rant/
.. _"Cores don't like to share": http://fgiesen.wordpress.com/2013/01/31/cores-dont-like-to-share/
.. _"Fixing cache issues, the lazy way": http://fgiesen.wordpress.com/2013/02/01/fixing-cache-issues-the-lazy-way/
.. _`"Frustum culling: turning the crank"`: http://fgiesen.wordpress.com/2013/02/02/frustum-culling-turning-the-crank/
.. _"The barycentric conspiracy": http://fgiesen.wordpress.com/2013/02/06/the-barycentric-conspirac/
.. _"Triangle rasterization in practice": http://fgiesen.wordpress.com/2013/02/08/triangle-rasterization-in-practice/
.. _"Optimizing the basic rasterizer": http://fgiesen.wordpress.com/2013/02/10/optimizing-the-basic-rasterizer/
.. _"Depth buffers done quick, part 1": http://fgiesen.wordpress.com/2013/02/11/depth-buffers-done-quick-part/
.. _"Depth buffers done quick, part 2": http://fgiesen.wordpress.com/2013/02/16/depth-buffers-done-quick-part-2/
.. _"The care and feeding of worker threads, part 1": http://fgiesen.wordpress.com/2013/02/17/care-and-feeding-of-worker-threads-part-1/
.. _"The care and feeding of worker threads, part 2": http://fgiesen.wordpress.com/2013/02/25/the-care-and-feeding-of-worker-threads-part-2/
.. _"Reshaping dataflows": http://fgiesen.wordpress.com/2013/02/28/reshaping-dataflows/
.. _"Speculatively speaking": http://fgiesen.wordpress.com/2013/03/04/speculatively-speaking/
.. _"Mopping up": http://fgiesen.wordpress.com/2013/03/05/mopping-up/
.. _"The Reckoning": http://fgiesen.wordpress.com/2013/03/10/optimizing-software-occlusion-culling-the-reckoning/
.. _the damage is irreversible: http://www.alessonislearned.com/
.. _Github: https://github.com/rygorous/intel_occlusion_cull/
.. _blog branch: https://github.com/rygorous/intel_occlusion_cull/tree/blog

.. |CC0| image:: http://i.creativecommons.org/p/zero/1.0/88x31.png
