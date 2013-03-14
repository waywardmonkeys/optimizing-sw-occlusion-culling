Optimizing Software Occlusion Culling - index
#############################################
:date: 2013-02-17 15:33
:author: Fgiesen
:category: Coding

.. toctree::
   :hidden:

   write-combining-is-not-your-friend
   a-string-processing-rant
   cores-dont-like-to-share
   fixing-cache-issues-the-lazy-way
   frustum-culling-turning-the-crank
   the-barycentric-conspiracy
   triangle-rasterization-in-practice
   optimizing-the-basic-rasterizer
   depth-buffers-done-quick-part-1
   depth-buffers-done-quick-part-2
   care-and-feeding-of-worker-threads-part-1
   care-and-feeding-of-worker-threads-part-2
   reshaping-dataflows
   speculatively-speaking
   mopping-up
   the-reckoning

In January of 2013, some nice folks at Intel released a `Software
Occlusion Culling demo`_ with full source code. I spent about two
weekends playing around with the code, and after realizing that it made
a great example for various things I'd been meaning to write about for a
long time, started churning out blog posts about it for the next few
weeks. This is the resulting series.

Here's the list of posts (the series is now finished):

#. :doc:`write-combining-is-not-your-friend`, on typical write combining
   issues when writing graphics code.
#. :doc:`a-string-processing-rant`, a slightly over-the-top post that
   starts with some bad string processing habits and ends in a rant
   about what a complete minefield the standard C/C++ string processing
   functions and classes are whenever non-ASCII character sets are
   involved.
#. :doc:`cores-dont-like-to-share`, on some very common pitfalls when
   running multiple threads that share memory.
#. :doc:`fixing-cache-issues-the-lazy-way`. You could redesign your
   system to be more cache-friendly - but when you don't have the time
   or the energy, you could also just do this.
#. :doc:`frustum-culling-turning-the-crank` - on the other hand, if you
   do have the time and energy, might as well do it properly.
#. :doc:`the-barycentric-conspiracy` is a lead-in to some in-depth posts
   on the triangle rasterizer that's at the heart of Intel's demo. It's
   also a gripping tale of triangles, Möbius, and a plot centuries in
   the making.
#. :doc:`triangle-rasterization-in-practice` - how to build your own
   precise triangle rasterizer and *not* die trying.
#. :doc:`optimizing-the-basic-rasterizer`, because this is real time, not
   amateur hour.
#. :doc:`depth-buffers-done-quick-part-1` - at last, looking at (and
   optimizing) the depth buffer rasterizer in Intel's example.
#. :doc:`depth-buffers-done-quick-part-2` - optimizing some more!
#. :doc:`care-and-feeding-of-worker-threads-part-1` - this project
   uses multi-threading; time to look into what these threads are
   actually doing.
#. :doc:`care-and-feeding-of-worker-threads-part-2` - more on
   scheduling.
#. :doc:`reshaping-dataflows` - using global knowledge to perform local
   code improvements.
#. :doc:`speculatively-speaking` - on store forwarding and speculative
   execution, using the triangle binner as an example.
#. :doc:`mopping-up` - a bunch of things that didn't fit anywhere else.
#. :doc:`the-reckoning` - in which a lesson is learned, but `the damage is
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
.. _the damage is irreversible: http://www.alessonislearned.com/
.. _Github: https://github.com/rygorous/intel_occlusion_cull/
.. _blog branch: https://github.com/rygorous/intel_occlusion_cull/tree/blog

.. |CC0| image:: http://i.creativecommons.org/p/zero/1.0/88x31.png
