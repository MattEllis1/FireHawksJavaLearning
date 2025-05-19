# Java Programming Activity: Coral Tracking in ReefScape!

Welcome, FireHawks! Today, you'll embark on a beginner-level Java coding adventure inspired by this season's game, ReefScape. In this activity, you'll use **Java arrays** to simulate scoring Coral on the Reef. Let's dive into the world of Coral placement and make sure the Reef is packed with valuable Coral for those points!

---

## 🌊 Problem Statement:

Imagine you are writing code to track Coral scored on the 4 levels of a Reef. Each level can hold **up to 12 Coral pieces**, and scoring Coral earns points based on the level:

- **Level 1 (L1):** 2-point Coral
- **Level 2 (L2):** 3-point Coral
- **Level 3 (L3):** 4-point Coral
- **Level 4 (L4):** 5-point Coral

Your task is to:
1. **Create an array** to represent each level of the Reef and track the number of Coral scored on each level.
2. Implement logic to **add Coral** to a level if there’s space.
3. Write a function to calculate the **total score** based on the Coral tracked in your array for the Reef.

---

## ⚙️ Instructions:

### Step 1: Set Up the Reef
1. Create an integer array named `reef` to represent the 4 levels of the Reef.  
   - The array will have **4 elements**, where:
     - Index 0 is for Level 1
     - Index 1 is for Level 2
     - Index 2 is for Level 3
     - Index 3 is for Level 4
   - Each index stores the number of Coral pieces currently scored on that level.

2. Initialize the array so that all levels start with `0` Coral pieces.

---

### Step 2: Add Coral to the Reef
Write a method `addCoral(int level, int pieces)` that:
- Takes two parameters: 
  - `level`: The level (1–4) you want to add Coral to.
  - `pieces`: The number of Coral pieces you want to add.
- Checks if there’s enough space on the chosen level to add the Coral (maximum 12 pieces per level).
- Adds Coral to that level if there’s space and updates the array.
- Outputs a message if the level is full or if the number of requested pieces cannot fit.

---

### Step 3: Calculate the Score
Write a method `calculateScore()` to:
- Calculate the total score for the Reef based on the Coral stored in the array.
  - Points per piece: 
    - Level 1 = 2 points
    - Level 2 = 3 points
    - Level 3 = 4 points
    - Level 4 = 5 points
- Return the total score as an integer.

---

### Step 4: Write a Main Method
In the `main` method:
1. Call `addCoral` multiple times to simulate adding Coral to different levels.
2. Print out the current state of the Reef after each addition.
3. Call `calculateScore` at the end and print out the total score.

---

## 📝 Example:
Here’s what a sample session might look like:

```plaintext
[INFO] Adding 12 Coral to Level 1...
[INFO] Reef state: [12, 0, 0, 0] 

[INFO] Adding 5 Coral to Level 2...
[ERROR] Cannot add 5 Coral to Level 2. Only a maximum of 12 Coral are allowed per level.

[INFO] Adding 6 Coral to Level 3...
[INFO] Reef state: [12, 0, 6, 0]

Total Score: 48
```

---

## 🧑‍💻 Starter Code:
Below is the skeleton code to get started. Complete the missing methods based on the instructions.

```
public class ReefScapeCoralTracker {

    // Array to track Coral on the Reef levels
    static int[] reef = {0, 0, 0, 0}; // Tracks Coral for L1, L2, L3, L4

    public static void main(String[] args) {
        // Simulate adding Coral and calculate the score
        addCoral(1, 12); // Example: Adding 12 Coral to Level 1
        printReefState();

        addCoral(3, 6); // Example: Adding 6 Coral to Level 3
        printReefState();

        int score = calculateScore(); // Calculate total score
        System.out.println("Total Score: " + score);
    }

    // Method to add Coral to a level
    public static void addCoral(int level, int pieces) {
        // TODO: Implement logic to check if Coral can be added (max capacity = 12).
        // If valid, add pieces to reef[level-1]. Print error message if level exceeds capacity.
    }

    // Method to calculate the total score
    public static int calculateScore() {
        // TODO: Implement logic to calculate score based on Coral pieces stored in reef array.
        // Multiply by appropriate level multipliers (e.g., 2 points for Level 1 Coral).
        return 0; // Replace with actual score calculation
    }

    // Method to print the current state of the Reef
    public static void printReefState() {
        System.out.println("[INFO] Reef state: " + java.util.Arrays.toString(reef));
    }
}
```

---

## 🚀 Challenges:
Modify the code to track scoring during the Autonomous Period, which applies bonus points to Coral (e.g., double points for all levels during Auton).
Write a method to compare and visualize scores between multiple Reefs (e.g., Reef 1 vs. Reef 2 in a multi-round simulation).

---

## 🎉 Ready to Rock the Reef?
Now it’s your turn! Customize the code, complete the missing methods, and see how high you can score. GO FIREHAWKS! 🚀
