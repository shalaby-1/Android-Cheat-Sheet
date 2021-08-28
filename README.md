# Android-Cheat-Sheet  
### global variable : defined outside a method  
### local variable : defined inside a method  
### What is 'Context' on Android?  
current state of the application/object. It lets newly-created objects understand what has been going on
### Steps to run app  
1- Sub class of `Activity` class is automatically created in java folder  
```java
public class MainActivity
```
2- `AppCompatActivity` is subclass of Android’s `Activity` class that provides compatibility support for older versions of Android  
```java
public class MainActivity extends AppCompatActivity 
```
3- we override one `Activity` method `onCreate(Bundle)` and it is called when an instance of the activity subclass is created  
```java
@Override
    protected void onCreate(Bundle savedInstanceState) 
```
4- we call this `Activity` method to get the UI related to this activity, this method inflates the layout and put it on the screen  
```java
setContentView(R.layout.activity_main);
```
### Resource  
is a piece of your application that is not code – things like image files, audio files, and XML files.  
