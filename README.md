# Training Track (logic)

This is an app that tracks training sessions to facilitate users the information about their training history. In this repo is expected to describe the data struct of the app and how it interact with the logic of the main features.

## Training Mindset
The app became useful in the “continuous improvement” training mindset, where it is desired to “improve” the performance of the training on each session. For that is useful to have quick access to historical data about the exercise that is about to be performed, so you don't have to remember how many reps you did last week on X exercise.  

Note that “continuous improvement” is not sustainable over time. Please contact a health professional before using this approach. 

## Business language

### Macrocycle
A macrocycle refers to a season of training in its entirety. Macrocycles are broken down into mesocycles.

### Mesocycle
It is a block where the training program is emphasized to achieve a goal, so the effort is focused on the same type of physical adaptations. It is composed of microcycles.

### Microcycle
It contains the training sets and rest days for that period, it is the smallest block and it usually lasts 1 week. Microcycles can have 2 focuses:
* Accumulation phase 
* Discharging

### Training set
Contain a collection of exercises within the range of reps recommended for the session


## Features

### Info about exercise in the previous microcycle. 

**Given** a mesocycle , **When** the athlete checks for one specific exercise in the current microcycle; **Then** the app should show how many reps the athlete did for that exercise in the last microcycle

```
Example:
rep1 -> 11(1)
rep2 -> 11(1)
rep3 -> 10(0)
```

### Info about exercise in the current mesocycle.

**Given** a mesocycle, **When** the athlete check for one specific exercise in the current microcycle; **Then** the app should show the historical of that exercise in the current mesocycle:

```
microcycle 1 -> 10(2)/9(2)/10(0)
microcycle 2 -> 11(1)/11(1)/10(0)
```

