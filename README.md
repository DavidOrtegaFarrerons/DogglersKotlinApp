# Welcome to DogglersApp!

This app is the final project from Unit 2 of Android Basics in Kotlin given by Google codelabs: https://developer.android.com/courses/android-basics-kotlin/course


# What is it about?

Dogglers app uses a RecyclerView in horizontal, vertical and grid view to show a group of CardViews with the dog image, name, age and hobbies.



## How has Dogglers app been done?

Dogglers app comes with some prebuilt-in code, so I had some specific tasks I had to accomplish in order to finish the project:

### Design part:

In this part of the project I had to make the xml designs for horizontal/vertical view and also for the grid one.

For the vertical/horizontal RecyclerView, I used the MaterialCardView with a ConstraintLayout inside it to place the information about the dog, here's the final design:

![Vertical/Horizontal dog cardivew design](https://i.imgur.com/BGN5hqS.png)

For the grid layout, using the same information as stated above, this is the design I came up with:

![Grid dog cardview design](https://i.imgur.com/uOZu1ev.png)


### Code part:

In the coding section, I had to implement the adapter in order to show the dogs in the frontend design I made before.

Firstly, I declared a variable called dogList which holds the list of dogs information.

![Imgur](https://i.imgur.com/8eELkFr.png)

Secondly, I created the class DogCardViewHolder, which extends from RecyclerView.ViewHolder. There I defined the different views we need to modify:
the dog image, and texts from name, age and hobbies.

![Imgur](https://i.imgur.com/dCYBl9r.png)

Thirdly, I implemented the onCreateViewHolder method from the DogCardViewHolder class (Which was inherited from its parent class RecyclerView.ViewHolder). For this scenario I had a problem, which was, what layout should I inflate (Vertical/Horizontal or Grid), for this, I used a when expression that checked whether the layout variable from the DogCardAdapter was Layout.Grid or any other value like Layout.Vertical or Layout.Horizontal. This can be seen in the Layout.kt file inside the const package.

![Imgur](https://i.imgur.com/CiKmmgp.png)

Fourthly i implemented the getItemCount() method which is trite.

![Imgur](https://i.imgur.com/mkyYD5Z.png)

Finally, the last step was to implement the onBindViewHolder() method which sets the different values across the ViewHolder UI items. The first thing I did was to get the current position dog that is holded in the dogData variable, then i set the image of the dog,  the name, the age, and the hobbies, always using the .? safe call operator for null-safety.

![Imgur](https://i.imgur.com/nG7HR4X.png)



## Final project overview

- Launcher app view:

![Imgur](https://i.imgur.com/b2apNk9.png)

- Vertical View:

![Imgur](https://i.imgur.com/Ol31Ty4.png)

- Horizontal View:

![Imgur](https://i.imgur.com/o4w6PII.png)

- Grid View:

![Imgur](https://i.imgur.com/wbsM0xm.png)
