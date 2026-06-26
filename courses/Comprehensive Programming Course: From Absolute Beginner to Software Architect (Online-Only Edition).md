# Comprehensive Programming Course: From Absolute Beginner to Software Architect (Online-Only Edition)

This course is designed for people with **zero programming experience** who cannot install software on their computers. You will use only **free online tools**—specifically, a browser-based Java development environment like **Replit** (replit.com). You will learn Java from the ground up, build a complete 3D board game (using JavaFX, available in Replit's JavaFX template), and understand software engineering principles—all without downloading anything.

## How to Use This Course

1. **Read each module** in order.
2. **Type every code example** into your online project and run it.
3. **Complete the practice exercises** – they reinforce what you learned.
4. **Build the project incrementally** – each module adds a new feature to your game.
5. **Ask questions** – use online forums or the course's discussion area.

---

## Module 0: Setting Up Your Online Development Environment

### 0.1 What You Need

- A modern web browser (Chrome, Firefox, Edge).
- A free account on **Replit** (https://replit.com) – sign up with email or Google.
- Notepad++ is optional; you can edit all code directly in Replit.

### 0.2 Create Your First Java Project on Replit

1. Log in to Replit.
2. Click the **"Create Repl"** button.
3. Choose **"Java"** as the language (not JavaFX yet – we'll use a special template later).
4. Give it a name, e.g., `MyFirstJava`.
5. Click **"Create Repl"**.

You will see a split screen: a file browser on the left, a code editor in the middle, and a console (output) on the right. The `Main.java` file is already open with a "Hello World" program.

### 0.3 Run Your First Program

The code in `Main.java` should look like:

```java
class Main {
  public static void main(String[] args) {
    System.out.println("Hello world!");
  }
}
```

Click the **"Run"** button. You should see `Hello world!` printed in the console.

**Congratulations!** You have just written and run your first Java program – entirely in your browser.

---

## Module 1: Java Basics – Variables, Data Types, and Input

### 1.1 What is Programming?

Programming is giving a computer a set of step-by-step instructions. A **program** is like a recipe. Java is one of the most popular languages because it runs on almost any device.

**Key concepts**:
- **Statements** – instructions that end with a semicolon (`;`).
- **Variables** – containers that store data.
- **Data types** – define what kind of data a variable can hold.

### 1.2 Variables and Data Types

Java has two categories of data types: **primitive** (simple values) and **reference** (objects like strings).

**Primitive types**:

| Type | Description | Example |
|------|-------------|---------|
| `int` | whole number | `int score = 100;` |
| `double` | decimal number | `double price = 19.99;` |
| `boolean` | true/false | `boolean gameOver = false;` |
| `char` | single character | `char grade = 'A';` |

**Reference type** (we use often): `String` (text).

```java
String name = "Alice";
```

**Naming rules**:
- Start with a letter, underscore, or `$`.
- Use **camelCase** for variables: `playerScore`, `isGameOver`.

### 1.3 Printing to the Console

```java
System.out.println("Hello");  // prints and moves to next line
System.out.print("World");    // prints without newline
```

### 1.4 Reading User Input

To read input from the user, we use a `Scanner`.

```java
import java.util.Scanner;  // must be at the top

public class InputDemo {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter your name: ");
        String name = scanner.nextLine();
        System.out.println("Hello " + name);
    }
}
```

### 1.5 Your First Project Step: Text-Based Menu

Let's start building our game – a text-based menu that will later become graphical.

Create a new Repl (Java) called `KnowledgeQuest`. Replace the code with:

```java
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int choice = 0;

        System.out.println("======================================");
        System.out.println("      WELCOME TO KNOWLEDGE QUEST      ");
        System.out.println("======================================");
        System.out.println("1. Start Game");
        System.out.println("2. High Scores");
        System.out.println("3. Instructions");
        System.out.println("4. Exit");
        System.out.print("Enter your choice: ");

        choice = scanner.nextInt();

        if (choice == 1) {
            System.out.println("Starting game...");
        } else if (choice == 2) {
            System.out.println("High scores...");
        } else if (choice == 3) {
            System.out.println("Instructions: ...");
        } else if (choice == 4) {
            System.out.println("Goodbye!");
        } else {
            System.out.println("Invalid choice.");
        }
        scanner.close();
    }
}
```

Run it, test each option.

**Your Task**: Add a welcome message that asks for the player's name and greets them.

---

## Module 2: Control Flow – Decisions and Loops

### 2.1 The `if-else` Statement

Used to make decisions.

```java
int age = 18;
if (age >= 18) {
    System.out.println("Adult");
} else {
    System.out.println("Minor");
}
```

**Logical operators**:
- `&&` (and)
- `||` (or)
- `!` (not)

### 2.2 The `switch` Statement

Cleaner for multiple discrete values.

```java
int day = 3;
switch (day) {
    case 1: System.out.println("Monday"); break;
    case 2: System.out.println("Tuesday"); break;
    default: System.out.println("Other");
}
```

### 2.3 Loops

**`while` loop** – repeats while condition is true:

```java
int i = 0;
while (i < 5) {
    System.out.println(i);
    i++;
}
```

**`do-while`** – runs at least once:

```java
int i = 0;
do {
    System.out.println(i);
    i++;
} while (i < 5);
```

**`for` loop** – when you know the number of iterations:

```java
for (int i = 0; i < 5; i++) {
    System.out.println(i);
}
```

### 2.4 Random Numbers

```java
import java.util.Random;
Random rand = new Random();
int dice = rand.nextInt(6) + 1;  // 1..6
```

### 2.5 Project Step: Game Loop and Dice Roll

Modify your `Main.java` to keep showing the menu until the user chooses Exit. Add a "Roll Dice" option.

```java
while (choice != 4) {
    // print menu, read choice
    if (choice == 3) {
        int roll = rand.nextInt(6) + 1;
        System.out.println("You rolled a " + roll);
    }
    // ... other options
}
```

---

## Module 3: Object-Oriented Programming – Classes and Objects

### 3.1 What is OOP?

OOP models real-world things as **objects** that have **attributes** (data) and **behaviors** (methods). A **class** is a blueprint; an **object** is an instance.

### 3.2 Creating a `Player` Class

Create a new file in Replit: `Player.java`.

```java
public class Player {
    private String name;
    private int health;
    private int score;
    private int position;

    public Player(String name) {
        this.name = name;
        health = 100;
        score = 0;
        position = 0;
    }

    public void move(int steps) {
        position += steps;
        System.out.println(name + " moved to " + position);
    }

    public void takeDamage(int damage) {
        health -= damage;
        if (health < 0) health = 0;
    }

    public void addScore(int points) {
        score += points;
    }

    // Getters
    public String getName() { return name; }
    public int getHealth() { return health; }
    public int getScore() { return score; }
    public int getPosition() { return position; }

    @Override
    public String toString() {
        return name + " | HP:" + health + " | Score:" + score + " | Pos:" + position;
    }
}
```

### 3.3 Using the Player

In `Main.java`:

```java
Player player = new Player("Alice");
player.move(3);
player.addScore(10);
System.out.println(player);
```

### 3.4 Encapsulation

We made fields `private` and provided getters. This protects the data from being changed incorrectly.

### 3.5 Project Step: Board and BoardSquare Classes

Create `BoardSquare.java`:

```java
public class BoardSquare {
    private int position;
    private String type;    // "normal", "question", "bonus", "penalty"
    private String description;

    public BoardSquare(int pos, String type, String desc) {
        this.position = pos;
        this.type = type;
        this.description = desc;
    }

    // Getters...
}
```

Create `Board.java`:

```java
public class Board {
    private BoardSquare[] squares;

    public Board(int size) {
        squares = new BoardSquare[size];
        for (int i = 0; i < size; i++) {
            String type = "normal";
            String desc = "Just a square";
            if (i % 5 == 0) { type = "question"; desc = "Answer a question!"; }
            else if (i % 7 == 0) { type = "bonus"; desc = "Bonus points!"; }
            else if (i % 11 == 0) { type = "penalty"; desc = "Lose health!"; }
            squares[i] = new BoardSquare(i, type, desc);
        }
    }

    public BoardSquare getSquare(int pos) {
        if (pos >= 0 && pos < squares.length) return squares[pos];
        return null;
    }
}
```

In `Main`, when starting game, create a Board and a Player. After rolling dice, move player and check the square.

---

## Module 4: Inheritance and Interfaces

### 4.1 Inheritance

A child class inherits from a parent. Use `extends`.

```java
public class GameObject {
    protected int x, y;
    public void move(int dx, int dy) { x += dx; y += dy; }
}

public class Player extends GameObject {
    private int health;
    // ...
}
```

### 4.2 Abstract Classes

Cannot be instantiated; used as a base.

```java
public abstract class GameEntity {
    public abstract void interact(BoardSquare square);
}
```

### 4.3 Interfaces

A contract that classes must implement.

```java
public interface Drawable {
    void draw();
}
public class Player extends GameEntity implements Drawable {
    public void draw() { /* draw player */ }
}
```

### 4.4 Polymorphism

Treat objects of different types through a common superclass/interface.

```java
List<GameEntity> entities = new ArrayList<>();
entities.add(new Player("Alice", 0));
entities.add(new ComputerPlayer("Bot", 0, 1));
for (GameEntity e : entities) {
    e.interact(square);
}
```

### 4.5 Project Step: Refactor Game Entities

Create `GameEntity` abstract class with `interact()`. Make `Player` extend it. Create `ComputerPlayer` extends `GameEntity` with AI logic. In main, use polymorphism.

---

## Module 5: Collections and File I/O

### 5.1 ArrayList and HashMap

```java
import java.util.ArrayList;
import java.util.HashMap;

ArrayList<String> names = new ArrayList<>();
names.add("Alice");

HashMap<String, Integer> scores = new HashMap<>();
scores.put("Alice", 100);
```

### 5.2 Reading and Writing Files

```java
import java.io.*;

// Write
try (PrintWriter out = new PrintWriter(new FileWriter("scores.txt"))) {
    out.println("Alice,100");
} catch (IOException e) { e.printStackTrace(); }

// Read
try (BufferedReader in = new BufferedReader(new FileReader("scores.txt"))) {
    String line;
    while ((line = in.readLine()) != null) {
        String[] parts = line.split(",");
        scores.put(parts[0], Integer.parseInt(parts[1]));
    }
} catch (IOException e) { e.printStackTrace(); }
```

### 5.3 Project Step: HighScoreManager

Create `HighScoreManager` with methods to add, save, load, and get top scores.

---

## Module 6: Introduction to JavaFX – GUI

### 6.1 Switching to JavaFX on Replit

To use JavaFX, create a new Repl and choose the **"JavaFX"** template (it includes JavaFX libraries). Name it `KnowledgeQuestFX`.

The template has a `Main.java` with a basic JavaFX application.

### 6.2 Understanding JavaFX

- `Application` – main class.
- `Stage` – the window.
- `Scene` – content container.
- `Node` – any UI element.
- `StackPane`, `VBox`, etc. – layout panes.

### 6.3 Your First JavaFX Program

```java
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.layout.StackPane;
import javafx.stage.Stage;

public class Main extends Application {
    @Override
    public void start(Stage primaryStage) {
        Button btn = new Button("Click me");
        btn.setOnAction(e -> System.out.println("Clicked!"));

        StackPane root = new StackPane();
        root.getChildren().add(btn);

        Scene scene = new Scene(root, 300, 200);
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    public static void main(String[] args) { launch(args); }
}
```

### 6.4 Project Step: Build a Graphical Menu

Create a `MenuScene` class that returns a `Scene` with buttons: Start, High Scores, Instructions, Exit.

---

## Module 7: JavaFX Graphics and Images

### 7.1 Loading Images

```java
Image img = new Image(getClass().getResourceAsStream("/logo.png"));
ImageView imgView = new ImageView(img);
```

### 7.2 Canvas for Custom Drawing

```java
Canvas canvas = new Canvas(400, 300);
GraphicsContext gc = canvas.getGraphicsContext2D();
gc.setFill(Color.RED);
gc.fillRect(50, 50, 100, 100);
```

### 7.3 Project Step: Add Logo and Background

Add a logo image to your menu using `ImageView`. Use a `StackPane` to layer background image and buttons.

---

## Module 8: 3D Graphics with JavaFX

### 8.1 Setting Up 3D

JavaFX has a 3D API. You need a camera, lights, and 3D objects.

```java
Group root = new Group();
PerspectiveCamera camera = new PerspectiveCamera(true);
camera.setTranslateZ(-1000);

Box box = new Box(200, 200, 200);
PhongMaterial mat = new PhongMaterial(Color.BLUE);
box.setMaterial(mat);

root.getChildren().add(box);
Scene scene = new Scene(root, 800, 600, true, SceneAntialiasing.BALANCED);
scene.setCamera(camera);
```

### 8.2 Primitives

- `Box`
- `Sphere`
- `Cylinder`

### 8.3 Textures

```java
Image texture = new Image("file:texture.png");
PhongMaterial mat = new PhongMaterial();
mat.setDiffuseMap(texture);
```

### 8.4 Project Step: Build 3D Game Board

Create a `GameBoard3D` class that creates a 4x5 grid of `Box` objects, each with a different color or texture. Group them and add to the scene.

---

## Module 9: Animation and Interactivity

### 9.1 Transitions

```java
RotateTransition rt = new RotateTransition(Duration.seconds(2), box);
rt.setByAngle(360);
rt.play();
```

### 9.2 Mouse Events on 3D

```java
box.setOnMouseClicked(e -> {
    System.out.println("Box clicked!");
});
```

### 9.3 Project Step: Spinner and Game Logic

Create a `Sphere` as a spinner. On click, animate rotation and determine which quadrant it stops on. Implement dice rolling, piece movement, and square interaction.

---

## Module 10: Audio, Polish, Packaging

### 10.1 Audio

```java
AudioClip sound = new AudioClip(getClass().getResource("/click.mp3").toString());
sound.play();
```

### 10.2 CSS Styling

Create a `.css` file and apply:

```java
scene.getStylesheets().add(getClass().getResource("/style.css").toExternalForm());
```

### 10.3 Packaging

On Replit, you can download the project as a ZIP. Or use the "Share" link to distribute.

---

## Module 11: Software Architecture Principles

### 11.1 SOLID

- Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion.

Apply these to refactor your game.

### 11.2 Technical Debt

Keep code clean, refactor often.

---

## Module 12: Capstone – Final Polish and Monetization

- Complete all features.
- Test thoroughly.
- Add sound effects, polish UI.
- Create a business plan for selling your game (e.g., on itch.io).
- Package your game as a JAR file.

---

## Final Project: "Knowledge Quest" – The Complete Game

You will have built a 3D educational board game with:
- Graphical menu
- 3D board with 20 squares
- Spinner to select category
- Dice roll and piece movement
- Question system with multiple-choice
- Score tracking
- High scores saved to file
- Sound effects
- Professional CSS styling

**Congratulations!** You are now a software architect.

---

## Appendix: Online Resources

- **Replit** – https://replit.com
- **Java Documentation** – https://docs.oracle.com/en/java/
- **GIMP Online Alternatives** – Photopea (https://www.photopea.com) for image editing.

---

**This course is complete and self-contained. Go through each module, type every code example, and build your game step by step. Happy coding!**
