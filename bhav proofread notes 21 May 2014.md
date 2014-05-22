Proofreading
======

Rick Bosch || 21 May 2014

##page 1
###paragraph 1
 - "projective transformation" - no definition
 - problem with "world space" - the projective transformation of points in 3D space onto a 2D plane
 - "between cameras" - unclear, you did not talk about 'cameras' in previous statement - perhaps "from one 2D plane to another"
 - "can and will" - future tense
 - "modelling" - no definition (you have different types of models in this paper; 3D tower model, mathematical camera model,etc; be clear on which one you talk about)

###paragraph 2
 - goes straight into explanation, takes a while to see what you're talking about - short intro? "Figure 1 illustrates a typical pinhole camera model..."
 - what is a principal axis? no definition of what it represents.
 - still have a problem with "3D point in world space"seems a bit redundant  to say 3D AND world space - prefer "a point in 3D space"

###paragraph 3
 - maybe simpler to say "projective transformations using homogeneous coordinates are linear and are readily solved using matrix algebra" 

###paragraph 4
 - "resulting image coordinate" unclear - maybe define along the lines of "coordinate of a mapped point on the image plane"
 - "for the canonical case" unclear - is the case where the camera and world origins coincide called "the canonical case", or is it an example of "*a* canonical case"

##page 2#
###equation 5
 - why the Z's in the offset terms?

###intrinsic parameters
 - why not introduce K as the calibration matrix in the previous section, when you show how K is derived?
 - "intrinsics" careful of jargon - define before you shorten "intrinsic parameters (intrinsics for brevity)"
 - "extrinsics" - you have a section on this later. keep this section focused on defining the intrinsics, rather than defining what are *not* intrinsics.
 - "camera's pose" - no definition
 - "object" - you have been talking about generic points up till now. no previous discussion of an object. introduce it first, or "the object being mapped"

##page 3
###extrinsic parameters
 - "world frame is not concurrent... " - can be shortended to more technical "non-canonical cases" if you define "canonical" earlier 
 - "i.e." - elaborate a little more, are we still in normal R3 or we using Homogeneous coordantes now? - along the lines of "this is a transformation between two Eucledian R3  spaces and can therefore be represented simply by a rotation R and translation t"
 - "pose" and" position" in this paragraph - it was "pose" and "orientation" in the paragraph on Intrinsic params
 - "inhomogeneous" - you defined "homogeneous", but does "inhomogeneous" specifically mean Euclidean? 
 - "3-vector" - no definition

###equation 8
 - matrix maths doesn't make sense - [2x2] * [4x1] - shouldn't it be [1x4] * [4*1]?
 - X is a homogeneous vector here [X,Y,Z,1]... contradicting the above "inhomogeneous 3-vector" statement
 - 3 X's in there, all different - confusing to have X_cam (ordinate defining camera X-axis?), X (the world-space ordinate?) and X (homogeneous vector to point in world space?)


##general notes
 - why are you using a pinhole camera model? is it worth presenting different kinds of models for background?

##page 4
###paragraph 1
 - "arrived at" - "determined"
 - "constrained" - vague
 - "To begin understanding..." - "Epipolar geometry can be considered as follows:"

###paragraph 2
 - "Figure 3 depicts a 3D point, X, being mapped onto the respective image planes of two pinhole cameras. The line connecting the camera centers is termed the _baseline_.
 - no x', C or C' in figure 3
 - "serve as epipoles which are" - "are named/termed/defined as epipoles, and are"

###figure 3
 - label vague - "Epipolar geometry of 2 pinhole cameras and a point in 3D space"

##page 5
###paragraph 1
 - "epipolar line" - no definition
 - "for an image point x..." - unclear - something along the lines of "for an image point x on one image plane, it's corresponding points x' and e' on another image plane form a line l' named an _epipolar_ line. Practically, this means that all points on one image plane will map to lines on all other image planes." 
 - "between X and x" - do x' and e' not correspond to X and C respectively? line X-C is the same line as X-x, but the word "between" makes me look at a line _segment_ and they are not the same segments

###fundamental matrix
 - "obeys the laws of" - "is the transformation matrix that provides the epipolar mapping of a point x in one image plane to it's respective line l' in another image plane.
 - "transformed via plane pi" - unclear. did not understand.
 - "homographic mapping" - no definition.
 - "the critical requirement" - vague. don't know why it's critical, so no reason to accept that plane Pi not intersecting the image plane is 'sufficient'.

##page 6
 - here you don't explain much and lose me in the maths quickly
 - "projective operator" - no definition

###paragraph after equation 14
 - "solved for up to scale" - don't know what "up to scale" means
 - un-explained, mass-information on *F*; super confusing

 - "F is a projective map... image." - should be at the beginning of the section

###essential matrix
 - "For a known camera *P* and in the event..." - "for a camera, whose camera matrix *P* and intrinsics *K* are known"
 - "undoing K" - jargon, don't know what undoing means
 - don't understand how normalizing x allows you to get the normalized P matrix
 - "Now considering..." - "In the special case where normalized cameras and normalized coordinates are used, the fundamental matrix attained is termed the _essential matrix_
 - "this first camera" - are you making reference to the figure? if so, say so.
 - "...two images, meaning that coplanar..." - "...two images. Using coplanar..."
 - say that E is the essential matrix

##page 7
 - "quantifiable a rotation" - grammar
 - "a simple check..." - unclear, confused on how to do the check
 - "For E=..." - is this an example or an important case?
