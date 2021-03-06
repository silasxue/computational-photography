/*****************************************************************************************************************/

********************************** COMPUTATIONAL PHOTOGRAPHY ASSIGNMENT 10 *****************************************
NAME : 		ADITYA VORA
ROLL NUMBER :	14410006
DEPARTMENT :	ELECTRICAL ENGINEERING


PROBLEM
------------------------------------------------------------------------------------------------------------------------
Given a set of multi-exposure images of a dynamic scene captured using a static camera, design an algorithm to generate the tone mapped HDR image of the scene without any ghosts.


IMAGES : Stack of images of a dynamic scene because of which the images in the stack are not aligned.

FILES:
assignment10.m = This is the main function that implements the entire algorithm. It takes the images as input and then divides the 
image into patches of a definate size. Then each patch is measured w.r.t reference patch whether it is consistent or not. Then the 
patches that are consistent are used finally in order to create the HDR image.

FUNCTION FILES: 
divideBlocks.m = This function takes the image from the stack as input and divides the image into blocks of appropriate size given as 
		 input.

getsamples.m = This function samples the stack of images to get few pixels from the stack which are then used to solve a 
		optimization problem to get the camera response function.

gsolve.m = This function solves the optimization problem in order to get the camera response function.

poisson_solver_function_neumann.m = Solves the poisson equation.[1][2]


--------------------------------------------------------------------------------------------------------------------------
REFERENCES:
[1] A. Agrawal, R. Raskar and R. Chellappa, "What is the Range of Surface Reconstructions from a Gradient Field? European Conference on
    Computer Vision (ECCV) 2006.
[2] A. Agrawal, R. Chellappa and R. Raskar, "An Algebraic approach to surface reconstructions from gradient fields?
    Intenational Conference on Computer Vision (ICCV) 2006.
