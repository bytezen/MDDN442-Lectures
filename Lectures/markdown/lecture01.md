
title: MDDN 442 - Lecture I
subtitle: 0503.13
class: title-slide


# Agenda
* Course Intro
	* Syllabus
	* Admin: Piazza
	* Your Interests
	* Course Breakdown
* Workshops 1-2
* Lecture 1

---

title: MDDN442 Overview
build_lists: true

* Goals:
	* Have fun
	* Do some cool shit
	* Professional level creative coding of computer graphics installations
	* Hone your research interests
	* Show work and expand your portfolio

---

title: Syllabus
build_lists: true

* Course divided into Workshops and Projects
* Workshops (30%) (minimum 5 hour homework __challenges__)
* Projects:
	* Midterm (30%)
	* Final (40%)
	* individual / group
	* your / class interests

---

title: Your interests...

__???__


#### note
 * What are you interests?
 * What if any creative coding tools are you familiar with? 


---

title: Your interests...

* what do you know?
* what do you want to learn?
* what do you want to learn better?
* what are you researching?

#### note
 * list some topics of interests
 * why are you taking this class

---

title: Our Challenge: Building Tech Skillz
content_class: flexbox vcenter

![makers discource tech](assets/makers_discourse_tacit.png)


---

title: A Media Design Framework
content_class: flexbox vcenter

![makers discource ](assets/makers_discourse.png)


---

title: The CG Media Design Trap
content_class: flexbox vcenter

![makers discource tech](assets/makers_discourse_tech.png)


---


### Become a professional amateur  
#### Learn to learn, invent and engage...fast

---

title: Workshop 1
subtitle: hand-in 12.03

"Prepare a 10 minute presentation of your portfolio"

* Be prepared to address questions about the work (technical and conceptual)
* Hand in documenation of the presented work to the tutor drive

---

title: Creative Coding ???
build_lists: true

* Loosely defined as coding tools for artists.
* Of course any code can be deployed by artists and used creatively.

#### note
* What is creative coding
* Can you name some Creative coding tools?
* What have you used?
* coding tools built for artists and used by artists

---

title: Creative Coding Tools / Frameworks
content_class: smaller

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

title: What is Interactivity ???

#### note
	How do you define interaction in terms of this class

---

title: What is Interactivity ???

* We are going to use an expansive definition

interactive graphics 
:	an external __signal__ that controls the rendering of digital content

* examples:
	* data
	* humans
	* transducers
	* controllers

---

title: Our weapons of choice
build_lists: true

* Language:
	* C++ 
* APIs:
	* OpenGL, GLSL, WebGL ???
* Framework:
	* __Cinder__
* Technologies:
	* Midi, OSC, Syphon, Spacebrew(?), ???	

---

title: Why Cinder?
class: smaller
build_lists: true

* Cinder will make you smarter
* Cinder will make you hotter
* Cinder will make you run faster
* "come on everyone is doing it..."  
"I'll be your best friend..."  
"what are you chicken..."  
...other favorite peer pressure lines

---

title: Why Cinder?
subtitle: Abstraction 

* Abstracts Native windowing systems ( OS X, Windows, iOS )
* Abstracts OpenGL...

---

title: Why Cinder?
subtitle: Abstraction OpenGL
class: smaller
build_lists: true

* OpenGL:	
	<pre class="pretty-print" data-lang="c++">
		glEnableClientState( GL_VERTEX_ARRAY );
		glVertexPointer( 2, GL_FLOAT, 0, lineVerts );
		lineVerts[0] = start.x; lineVerts[1] = start.y;
		lineVerts[2] = end.x; lineVerts[3] = end.y;
		glDrawArrays( GL_LINES, 0, 2 );
		glDisableClientState( GL_VERTEX_ARRAY );
	</pre>

* Cinder:
	<pre class="pretty-print" data-lang="c++">
		gl::drawLine();
	</pre>

#### note
* Level of familiarity with OpenGL
* Which version 

---

title: Why Cinder?
build_lists: true

* C++ is hard ( but we are tough sons-of-bitches )
	* [A Zen Moment in C](http://markshroyer.com/2012/06/c-both-true-and-false/)
* C++ is closer to the mettle of the hardware
* Many systems still use C++
	* C++ gets you closest to the most hardcore systems...build up ( abstract ) from there
* Learning new languages in a non-creative context is often frustrating because the content is misscoped
* Learning in a group and leveraging experiences is fun and easier

#### note
* take home message from Zen Moment in C __INITIALIZE YOUR VARIABLES!!__

---

title: Why Cinder?

* The community is awesome, strong and high profile  
* The code is architected very well

#### example
[mouse callback example site:libcinder.org](https://www.google.co.nz/search?q=mouse+callback+example+site%3Alibcinder.org&aq=f&oq=mouse+callback+example+site%3Alibcinder.org&aqs=chrome.0.57.11722j0&sourceid=chrome&ie=UTF-8)

#### note
* Paul Houx is a very active member of the community. Here you see one of his first posts...
* Discussion about framework organization decisions...
* Discussion on strategies for architecting C++ code
	* [SJBaker C++ Headers Wiki](http://www.sjbaker.org/wiki/index.php?title=C%2B%2B:_multiple_source_files)


---

title: Why Cinder?

* Differentiate yourself in the marketplace
	* Work at Disney 
		* [Tron](http://jtnimoy.net/workviewer.php?q=178)
	* IBM THINK 
	* [KeimWeisshaar](http://www.kramweisshaar.com/)

#### note
* Stop KeimWeisshaar example at 40sec
* Run IBM THINK examples from desktop


---

title: Workshop 2
subtitle: due 12.03

1. Get Cinder installed. Use the Git version
2. Get yourself setup on Git
3. Go through Robert Hodgins Welcome to Cinder tutorial
4. Make some changes to the tutorial
5. Turn your app into the Tutor drive (upload to Piazza?)

---

title: Let's Get Started - OpenGL...
class: seque


---

title: OpenGL
build_lists: true

OpenGL:
	A set of APIs to interface with graphics hardware

* manages GPU resources to render image
* low-level geometric primitives: points, lines, polys
* higher level objects are managed by external frameworks (e.g. GLU, Cinder, Processing, PyGL, etc.)
* windowing operations and I/O are managed by external frameworks
* hardware and OS independent. Cross platform???	
	* GL Version detection via:
		* [GLView](http://www.realtech-vr.com/glview/)


---

title: OpenGL
build_lists: true

* OpenGL is a State Machine
	* Set flags that configure the state
	* Send Primitives to be rendered
	* Clear state
	* Repeat
* The applications tells the card how to draw primitives via state variables
* When drawing the card uses the current state to determine how primitives are drawn

---

title: OpenGL

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

title: OpenGL - Application Overview
build_lists: true

* Setup:
	* Create a window and bind OpenGL to it
	* Setup Event handlers (e.g. window resize)
	* Setup the drawing canvas
	* Prepare canvas for rendering with state variables
* Draw: 
	* clear framebuffer
	* screen coordinate mapping (optional)
	* change projection matrix (if necessary)
	* set up lights and camera
	* draw primitives
	* ...render....

---

title: OpenGL Pipeline
class: smaller
content_class: flexbox vcenter

![Pipeline Example](assets/visualpipeline.gif)

---

title: OpenGL Pipeline
content_class: flexbox vcenter

![Pipeline](assets/pipeline.gif)

### Vertex Transformations

* In: vertex positions
* In: lighting positions per vertex
* Out: generation and transformation of texture coordinates

#### note
* The inputs to the vertex transformation are the vertices and per vertex attributes,  
	like color, normals, tex coords.


---

title: OpenGL Pipeline
class: smaller
content_class: flexbox vcenter

![Pipeline Example](assets/visualpipeline.gif)

---

title: OpenGL Pipeline
content_class: flexbox vcenter

![Pipeline](assets/pipeline.gif)

### Primitive Assembly / Rasterization

* In: transformed vertices
* In: connectivity information
* Out: Fragment positions, and interpolated fragment attributes

#### note
* Model, View and Projection matrices are used to transform the vertices

---
title: OpenGL Connectivity Types
content_class: flexbox vcenter

![Connectivity](assets/geometricPrimitiveTypes.gif)

---

title: OpenGL Pipeline
class: smaller
content_class: flexbox vcenter

![Pipeline Example](assets/visualpipeline.gif)

---

title: OpenGL Pipeline
content_class: flexbox vcenter
class: smaller

![Pipeline](assets/pipeline.gif)

### Fragment Texturing and Coloring

* In: interpolated color and TexCoords for pixels in fragment
* In: Texel information
* In: Fog
* Out: Color value and depth value per fragment

---

title: OpenGL Pipeline
class: smaller
content_class: flexbox vcenter

![Pipeline Example](assets/visualpipeline.gif)

---

title: OpenGL Pipeline
class: small
content_class: flexbox vcenter

![Pipeline](assets/pipeline.gif)

### Raserization

* In: pixel location
* In: fragment color and depth 
* In: tests -> scissor test, alpha test, stencil test, depth test
* Out: pixel color based on tests and blend mode

---

title: OpenGL Pipeline
class: smaller
content_class: flexbox vcenter

![Pipeline Example](assets/visualpipeline.gif)

---	

title: Ignore the previous 4 slides...sort of

* Cinder abstracts the goryness of OpenGL away
* However, when you need to know something, change something, learn something the Cinder source is a great place to visit
	* gl::  
	example: 
	<pre>
	</pre>

---

title: Cinder

* [Download Cinder](http://libcinder.org/docs/welcome/GitSetup.html)
	* follow instructions to build Cinder
* Open the "_AllSamples" project
* Open the "basicApp" (32bit version)

---
title: Cinder - Basic App

<pre class="pretty-print" data-lang="c++">
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
content_class: smaller

<pre class="pretty-print" data-lang="c++">
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

#### note
* Note gl:: namespace calls mixed with openGL calls
* Note OpenGL setMatricesWindow call. What is that doing?
* glBegin... equivalent to <pre>beginShape()</pre> in Processing



---
title: OpenGL Matrices and back to Linear Algebra
content_class: smaller

<pre class="pretty-print" data-lang="c++">
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



---
title: OpenGL Matrices and back to Linear Algebra


* Open the Cinder Source for hints!
* cinder::gl
* refreshers:  
	* [OpenGL Matrix Overview](http://www.opengl-tutorial.org/beginners-tutorials/tutorial-3-matrices/)
	* [Intuitive Guide to Linear Algebra](http://betterexplained.com/articles/linear-algebra-guide/)
	* [Matrices Can Be Your Friend](http://www.sjbaker.org/steve/omniv/matrices_can_be_your_friends.html)


---
title: Cinder AppBasic

* App -> AppBasic -> __<your App>__
* You can learn what is capable by browsing the header files	
	* AppBasic.h
	* App.h

#### note
In App.h point out:
- CallbackId registerXXXXX()
- timeline()
- copyWindowSurface()


---
title: Cinder Tut
subtitle: creating your first app


1. Tinderbox (first time requires path to Cinder)
2. How to add Callbacks ??
	* [mouse callback example site:libcinder.org](https://www.google.co.nz/search?q=mouse+callback+example+site%3Alibcinder.org&aq=f&oq=mouse+callback+example+site%3Alibcinder.org&aqs=chrome.0.57.11722j0&sourceid=chrome&ie=UTF-8)
	* There is a Listener Example!

#### note
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




