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
### Getting references to widgets  
In an activity, you can get a reference to an inflated widget by calling the following `Activity` method:
```java
public View findViewById(int id)
```
This method accepts a resource ID of a widget and returns a View object.
example of usage  
```java
public class QuizActivity extends AppCompatActivity {
private Button mTrueButton;
private Button mFalseButton;
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_quiz);
mTrueButton =  findViewById(R.id.true_button);
mFalseButton =  findViewById(R.id.false_button);
}
}
```
### Android Applications are Event Driven Applications
Unlike command-line programs or scripts, event-driven applications start and then wait for an event, such as the user pressing a button. 

