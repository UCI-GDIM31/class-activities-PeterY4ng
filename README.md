# in-class-activities
## Devlogs
### W1
Hello World! £º£©

### W2
Create future Devlog sub-headers with the three # symbols, then write your Devlogs below them.
### Devlogs
r, g, and b are float variables because they represent decimal values for colors, so they can't be integers, booleans, or strings. The _bounces variable is an integer because the number of times a ball bounces can only be a whole number, not a decimal, boolean, or string. The error I encountered in Step 4 of Part 2 was "Assets\W2\Scripts\Ball.cs(67,18): error CS1002: ; expected", which means I didn't add a ";" at the end of that line of code, making it incomplete.

### W3
Table 19
as player¡¯s sanity level becomes lower, the light will become dimmer, and the light itself is void because the light is depending on player¡¯s sanity level
1.We can liken a class to an "architectural drawing", and a Component to an "actual building" constructed according to the drawing. A class, as a template, is like a drawing that specifies the overall style and structure of a building; when a class is attached to a game object, it becomes a component, just as a specific building is built according to the drawing. Member variables are like the "traits" of a building, such as the height, color, and number of windows of the building, which are the properties of each class (drawing). Methods are what the building can "do", such as providing accommodation for people, being used for commercial office work, and withstanding certain wind and rain, that is, the behavioral capabilities of the class.
2.Because in Step 8 and Step 9, we kept changing the ball's (related) variable but didn't set an upper limit, so the ball will become brighter and brighter.

### W4
Table 19
line 17 is declearing a variable, is a ture or false varible, its type is boolean.	A basic C# data type which stores a true or false value.
line 28 is A C# statement used to branch between different lines of code. The code inside the brackets of an if statement will only be executed if the conditions inside the parentheses are met.
to detect whether the player is grounded or not, and whether the player press the space
line 32 is a ture or false varible, its type is boolean. Means when cat is not grounded, its state will become fales, in order to preven the player from double jumping

The method I came up with is to add rigid bodies to the kitten, the football, and the goal because they are all objects affected by physics. I locked the XYZ rotation and position of the goal because the goal doesn't move at all. (Later I learned that actually setting the goal's rigid body like this is not much different from having no rigid body at all.) Both the football and the kitten need to have rigid bodies because they will collide with each other. I set "Is Trigger" on for the goal because the goal should be able to add points when the ball passes through it. When I tested the game for the first time, every time the football rolled to the edge, it would just fall off, but later I added the "Bounce Off the Wall" component to the football, and then the football wouldn't fall off.

### W5
I am not quite understand what is Getcomponent
my classmates tood me that it is used to get other components that are attached to the same game object. For example, in the player controller script, we use Getcomponent to get the rigidbody component of the player game object so that we can apply forces to it and make it move. I also learned that Getcomponent can be used to get components from other game objects by using GameObject.Find() to find the game object first, and then using Getcomponent on that game object.

I think for the member variables, we need Need a NavMeshAgent variable (for navigation), an Animator variable (for animation control), a float variable for movement speed
Need Unity-provided methods like Start() (initialize variables), Update() (update logic every frame)
For start(), When the script starts, initialize NavMeshAgent, Animator, and set the initial state and movement speed.
For update(), Continuously check for player input, update the character's movement and animation based on the input and NavMeshAgent's state.

I had been having some trouble with the step of making the deer move on its own. No matter how I modified my code, the deer just stood still. Later, I asked LA, and she told me that I should drag the script of the deer into the deer's Inspector. After doing that, I finally solved my problem.

### W6
URL
https://docs.google.com/document/d/13WL1faOUeHHIt5U-4Nu450rY6-oTy8zhNi828PVl7UI/edit?tab=t.0
We are table 19, I am doing Unity engine

The chasing speed is set via the _speed variable, and the player's position is stored using _playerTransform. The EnableChase method is used to activate chasing and record the player as the target, while the DisableChase method is for deactivating chasing. We need to first define a class structure that inherits from MonoBehaviour, then set up variables for controlling speed and storing the player's position, followed by implementing methods to activate and deactivate chasing, and finally add the logic in BatManager to make the bat move towards the player.

## Open-Source Assets
### W1
- Animals: https://assetstore.unity.com/packages/3d/characters/animals/animals-free-animated-low-poly-3d-models-260727 
- Low-poly environment: https://assetstore.unity.com/packages/3d/environments/landscapes/low-poly-simple-nature-pack-162153 