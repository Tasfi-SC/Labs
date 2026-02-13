# CS2053 - Concept Assignment 1
## [Tasfi Samad Choudhury]

---

**1**:
Answer here

**2-a**:
_physics_process is a fixed step update where it runs at a constate frame rate set by the project eg 60FPS where as _process(delta) is the per render frame update and it runs every frame, ideally used for non physics gameplay update, UI, timers etc. Lastly, _ready() runs once when a node enters the scene tree and is finished setting itself up.The function is meant for initialization.
_ready() happens first once per node, when it becomes active in the scene tree. Then the engine repeatedly calls _physics_process() as many times required per display frame and then _process runs once per displayed frame.
**2-b**:
Godots game loop has to update the world and draw it. Godot splits the update into two parts. First the _physics_process() for stable stimulation and _process for a variable rate rendering for everything that should feel smooth at the display frame rate._ready() is used to set everything up before either update loop starts.
**2-c**:
We can control _process() and _physics_process() frequency by enabling and disabling whether the functions run for a given node or not but we cant directly set it to run a specific number of times. _ready() is not a repeating function
**3** 
Buffering is used in 2d games to set up the next frame off screen then swap it to the screen. This prevents players from seeing partically drawn frames and makes game animation smoother. A common reason to disable buffering is to reduce latency for time sensetive games. 
**4**:
A tileset is the collection of tiles we can use while tilemap is the gridbased level layout we use to paint using the tiles. 
**5-a**:
(6,6)
**5-b**:
Vector2 p1 = gameObject1.position
Vector2 p2 = gameObject2.position
Vector 2 direction = p2-p1

**6**:
We can consider charactor position as C and the explotion as E, so the direction of sound would be d = E-C. Then we would turn D into a unit vector by normalizing it D = d/||D|| . If D is positive sound comes from right, if D is negative from the left and D = 0 then we can use centered. 
**7-a**:
DotProduct(N,L) equalts to a cos(theta), where theta is the angle between the surface normal and the light direction. Diffusecolor represents what color it reflects under white light. Multiplying it by N.L allows us to scale that base color depending on how strongly the light is hitting based on the angle giving the final diffuse contribution. For a directional light without a light source position, L vector is normalized directional vector representing the direction from the surface point towards the light.
**7-b**:
DotProduct(R,V) is the angle between the reflection direction and viewer direction. SpecularColor is the material's specular tint. So multiplying pow(DotProduct(R, V)` with SpecularColor gives intensity of highlight based on view allignment.
**8-a**:
<9,12,2>
**8-b**:
<12,16,0>
**8-c**:
<-16,12,0>
**8-d**:
50
**9**:
|100|3|
|010|4|
|001|2|
|000|0|

**10**:
We filter the signal to make it more stable and usable for gameplay logic. Some ways to filter both are threshold,time-based filering,edge detection. 

---
