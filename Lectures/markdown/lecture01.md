
MDDN 442 - Lecture I
====================
0503.13

# Agenda

* Syllabus
* Your Interests
* Piazza
* Workshop 1-2
* Lecture 1

---

# Overview
* Goals:
	* Have fun
	* Do some cool shit
	* Professional level creative coding of computer graphics installations
	* Hone your research interests
	* Show work and expand your portfolio

---


# Syllabus
* Course divided into Workshops and Projects
* Workshops (30%) (minimum 5 hour homework __challenges__)
* Projects:
	* Midterm (30%)
	* Final (40%)
	* individual / group
	* your / class interests

---

<!--
 1. What are you interests?
 2. What if any creative coding tools are you familiar with? 
-->
# Your interests...

__???__

---

<!--
	list some topics of interests,
	why are you taking this class
-->
# Your interests...

* what do you want to learn
* what do you want to learn better

---

# The Maker's Challenge

![makers discources](assets/makers_discourse.jpg)

---

# The Maker's Challenge

* Professional Amateur
	* Learn to learn, invent and engage
	   ...fast

---

# Workshop 1
hand-in 12.03

"Prepare a 10 minute presentation of your portfolio"

* Be prepared to address questions about the work (technical and conceptual)
* Hand in documenation of the presented work to the tutor drive

---

<!--
	1. What is creative coding
	2. Can you name some Creative coding tools?
-->
# Creative Coding ???

* Loosely defined as coding tools for artists.
* Of course any code can be deployed by artists and used creatively.

---

# Creative Coding Tools / Frameworks

* [openFrameworks](http://www.openframeworks.cc)
* [Processing](http://processing.org)
* [Cinder](http://libcinder.org)
* [Field](http://openendedgroup.com/field/)
* [PureData](http://puredata.info)
* [Max/MSP/Jitter](http://cycling74.com/products/max)
* [Nodebox](http://nodebox.net)
* [vvvv](http://vvvv.org)
* [Touch Designer](http://www.derivative.ca)
* [Super Collider](http://http://supercollider.sourceforge.net/)
* [three.js](http://mrdoob.github.com/three.js)
* [Vuo](http://vuo.org)
* [Quartz Composer](http://developer.apple.com)
* [SpaceBrew](http://spacebrew.cc)

---

<!--
	How do you define interaction in terms of this class
-->
# What is Interactivity ???

---

# What is Interactivity ???
* We are going to use an expansive definition

interactive graphics 
:	an external signal that controls the rendering of digital content


* examples:
	* data
	* humans
	* transducers
	* controllers

---

# Our weapons of choice

* Technologies:
	* Midi, OSC, Syphon, Spacebrew ???
* Language:
	* WebGL, OpenGL, GLSL, ???
	* __Cinder__	

---

title: Why Cinder?
class: build_list smaller

* Cinder will make you smarter
* Cinder will make you hotter
* Cinder will make you run faster
* Come on everyone is doing it...  
	I'll be your best friend...  
	what are you chicken...  
	(other favorite peer pressure lines ???)

---

title: Why Cinder?
subtitle: Abstraction

* Cinder:
	<pre>
		gl::drawLine()
	</pre>

* OpenGL:	
	<pre>
		glEnableClientState( GL_VERTEX_ARRAY );
		glVertexPointer( 2, GL_FLOAT, 0, lineVerts );
		lineVerts[0] = start.x; lineVerts[1] = start.y;
		lineVerts[2] = end.x; lineVerts[3] = end.y;
		glDrawArrays( GL_LINES, 0, 2 );
		glDisableClientState( GL_VERTEX_ARRAY );
	</pre>

* Abstracts Native windowing systems ( OS X, Windows )

---

title: Why Cinder?

* C++ is hard but we are tough sons-of-bitches  
	[A Zen Moment in C](http://markshroyer.com/2012/06/c-both-true-and-false/)
* C++ is closer to the mettle of the hardware
* Many systems still use C++ and this will get you closest to the most hardcore systems...build up from there
* Learning new languages in a non-creative context is often frustrating because the content is misscoped
* Learning in a group and leveraging experiences is fun and easier

---

title: Why Cinder?

<!--
	* Paul Houx is a very active member of the community. Here you see one of his first posts...
	* Discussion about framework organization decisions...
	* Discussion on strategies for architecting C++ code
		* [SJBaker C++ Headers Wiki](http://www.sjbaker.org/wiki/index.php?title=C%2B%2B:_multiple_source_files)

-->

* The community is awesome, strong and high profile  

[mouse callback example site:libcinder.org](https://www.google.co.nz/search?q=mouse+callback+example+site%3Alibcinder.org&aq=f&oq=mouse+callback+example+site%3Alibcinder.org&aqs=chrome.0.57.11722j0&sourceid=chrome&ie=UTF-8)


---

<!--
	Run IBM THINK examples
-->
# Why Cinder?

* Differentiate yourself in the marketplace
	* Work at Disney [Tron](http://jtnimoy.net/workviewer.php?q=178)
	* IBM THINK 
	* [KeimWeisshaar](http://www.kramweisshaar.com/)

---

title: Workshop 2
subtitle: 12.03


1. Get Cinder installed. Use the Git version
2. Get yourself setup on Git
3. Go through Robert Hodgins Welcome to Cinder tutorial
4. Make some changes to the tutorial

---

Let's Get Started - OpenGL...
========

---

title: OpenGL


OpenGL:
	A set of APIs to interface with graphics hardware

* manages GPU resources to render image
* low-level geometric primitives: points, lines, polys
* higher level objects are managed by external frameworks (e.g. GLU, Cinder, Processing, PyGL, etc.)
* windowing operations and I/O are managed by external frameworks
* hardware and OS independent. Cross platform???	

---

title: OpenGL Pipeline

<!--
	The inputs to the vertex transformation are the vertices and per vertex attributes,  
	like color, normals, tex coords.
-->
![Pipeline](assets/pipeline.gif)

### Vertex Transformations

* In: vertex positions
* In: lighting positions per vertex
* Out: generation and transformation of texture coordinates

---

title: OpenGL Pipeline


![Pipeline](assets/pipeline.gif)

### Primitive Assembly / Rasterization

* In: transformed vertices
* In: connectivity information
* Out: Fragment positions, and interpolated fragment attributes

---

![Connectivity](assets/geometricPrimitiveTypes.gif)

---

title: OpenGL Pipeline
class: smaller


![Pipeline](assets/pipeline.gif)

### Fragment Texturing and Coloring

* In: interpolated color and TexCoords for pixels in fragment
* In: Texel information
* In: Fog
* Out: Color value and depth value per fragment

---

title: OpenGL Pipeline
class: small


![Pipeline](assets/pipeline.gif)

### Raserization

* In: pixel location
* In: fragment color and depth 
* In: tests -> scissor test, alpha test, stencil test, depth test
* Out: pixel color based on tests and blend mode

---

title: OpenGL Pipeline
class: smaller

![Pipeline Example](assets/visualpipeline.gif)

class: source

this is the source




---

# OpenGL

* OpenGL is a State Machine
1. Set flags that configure the state
2. Send Primitives to be rendered
3. Clear state
4. Repeat
* The applications tells the card how to draw primitives via state variables
* When drawing the card uses the current state to determine how primitives are drawn

* GL Version detection via:
[GLView](http://www.realtech-vr.com/glview/)

---

# OpenGL

* state variables:
	* background color
	* vertex color
	* camera position, orientation, FOV
	* ligthing (color, number, location)
	* drawing modes (points, lines, ) (e.g. Processing Begin Shape modes)
	* normal vectors
	* material properties
	* texture properties
	* depth, transparency, fog, antialiasing
	* viewing and projection matrices

---

# OpenGL - Application Overview

1. Create a window and bind OpenGL to it
2. Setup Event handlers (e.g. window resize)
3. Setup the drawing canvas
4. Prepare canvas for rendering with state variables
5. Draw Loop
	* clear framebuffer
	* screen coordinate mapping (optional)
	* change projection matrix (if necessary)
	* set up lights and camera
	* draw primitives
	* ...render....

---	

# Ignore the previous 4 slides...sort of

* Cinder abstracts the goryness of OpenGL away
* However, when you need to know something, change something, learn something the Cinder source is a great place to visit
	* gl::  
	example: 
	<pre>
	</pre>

---
title: Cinder

1. [Download Cinder](http://libcinder.org/docs/welcome/GitSetup.html)
	* follow instructions to build Cinder
2. Open the <pre>_AllSamples</pre> project
3. Open the <pre>basicApp</pre> (32bit version)

---
title: Cinder - Basic App

<pre class="c++">
class BasicApp : public AppBasic {
 public:
	// Cinder will always call this function whenever the user drags the mouse
	void mouseDrag( MouseEvent event );
	void keyDown( KeyEvent event );
	// Cinder calls this function 30 times per second by default
	void draw();

	// This will maintain a list of points which we will draw line segments between
	list<Vec2f>		mPoints;
};
</pre>


---
title: Cinder - Basic App

<!--
	* Note gl:: namespace calls mixed with openGL calls
	* Note OpenGL setMatricesWindow call. What is that doing?
	* glBegin... equivalent to <pre>beginShape()</pre> in Processing
-->

<pre class="c++">
void BasicApp::draw()
{
	gl::setMatricesWindow( getWindowSize() );
	// this pair of lines is the standard way to clear the screen in OpenGL
	gl::clear( Color( 0.1f, 0.1f, 0.1f ) );

	// We'll set the color to an orange color
	glColor3f( 1.0f, 0.5f, 0.25f );
	
	// now tell OpenGL we've got a series of points it should draw lines between
	glBegin( GL_LINE_STRIP );
	// iterate across our list of points, and pass each one to OpenGL
	for( list<Vec2f>::iterator pointIter = mPoints.begin(); pointIter != mPoints.end(); ++pointIter ) {
		glVertex2f( *pointIter );
	}
	// tell OpenGL to actually draw the lines now
	glEnd();
}
</pre>

---
title: OpenGL Matrices and back to Linear Algebra

* Open the Cinder Source for hints!
* cinder::gl

<pre class="c++">
void setMatricesWindow( int screenWidth, int screenHeight, bool originUpperLeft )
{
	glMatrixMode( GL_PROJECTION );
	glLoadIdentity();
#if defined( CINDER_GLES )
	if( originUpperLeft )
		glOrthof( 0, screenWidth, screenHeight, 0, -1.0f, 1.0f );
	else
		glOrthof( 0, screenWidth, 0, screenHeight, -1.0f, 1.0f );
#else	
	if( originUpperLeft )
		glOrtho( 0, screenWidth, screenHeight, 0, -1.0f, 1.0f );
	else
		glOrtho( 0, screenWidth, 0, screenHeight, -1.0f, 1.0f );
#endif
	glMatrixMode( GL_MODELVIEW );
	glLoadIdentity();
	glViewport( 0, 0, screenWidth, screenHeight );
}
</pre>

* refresher  
[OpenGL Matrix Overview](http://www.opengl-tutorial.org/beginners-tutorials/tutorial-3-matrices/)

---
title: Cinder AppBasic

<!--
	In App.h point out:
	- CallbackId registerXXXXX()
	- timeline()
	- copyWindowSurface()
-->

* App -> AppBasic -> __<your App>__
* You can learn what is capable by browsing the header files	
	* AppBasic.h
	* App.h

---
title: Cinder Tut
subtitle: creating your first app

<!--
	1. Run the Google Search for Call backs
	2. Note the Listener Example
	3. Open Listener and Run it
	4. Open the Code and see what is happening: __Note the Architecture!__
	5. Enter our version of the code:
		* member color
		* Member function
	6. Build with error in the color....
	7. Show how to look up the color in the documentation on Cinder. Strategies.
	8. Can't change the mouse color back??
	9. Use built in Cinder mouseHandlers
-->	

1. Tinderbox (first time requires path to Cinder)
2. How to add Callbacks ??
	* [mouse callback example site:libcinder.org](https://www.google.co.nz/search?q=mouse+callback+example+site%3Alibcinder.org&aq=f&oq=mouse+callback+example+site%3Alibcinder.org&aqs=chrome.0.57.11722j0&sourceid=chrome&ie=UTF-8)
	* There is a Listener Example!





