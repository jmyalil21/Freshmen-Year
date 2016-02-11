# Freshmen-Year
Code worked on during Freshmen Year at Thomas Jefferson High School for Science and Technology

Used in conjunction with Bumper, BumperPanel, BumperCollision, Polkadot, and PolkadotPanel with a Driver class as well

//Name:              Date:
   import java.awt.*;
    public class Ball extends Polkadot
   {
      private double dx;       // pixels to move each time step() is called.
      private double dy;
    // constructors
       public Ball()         //default constructor
      {
         super(200, 200, 50, Color.BLACK);
         dx = Math.random() * 12 - 6;          // to move vertically
         dy = Math.random() * 12 - 6;          // to move sideways
      }
       public Ball(double x, double y, double dia, Color c)
      {
         super(x, y, dia, c);
         dx = Math.random()* 12 - 6;
         dy = Math.random() * 12 - 6;
      }
      
     //modifier methods 
       public void setdx(double x)        
      {
         dx = x;
      }
       public void setdy(double y)
      {
         dy = y;
      }
      
      //accessor methods
       public double getdx()             
      {
         return dx;
      }
       public double getdy()
      {
         return dy;
      }
      
     //instance methods
       public void move(double rightEdge, double bottomEdge)
      {
         setX(getX()+ dx);                  // move horizontally
         setY(getY()+ dy);
        
         if(getX() >= rightEdge - getRadius())           {
            setX(rightEdge - getRadius());
            dx = dx * -1; 
         }
        /* more code goes here  */
         else if(getX() <= getRadius())           {
            setX(getRadius());
            dx = dx * -1; 
         }
        /* more code goes here  */
         else if(getY() <= getRadius())           {
            setY(getRadius());
            dy = dy * -1; 
         }
        /* more code goes here  */
         else if(getY() >= bottomEdge - getRadius())           {
            setY(rightEdge - getRadius());
            dy = dy * -1; 
         }
        /* more code goes here  */
         
      }
   }
