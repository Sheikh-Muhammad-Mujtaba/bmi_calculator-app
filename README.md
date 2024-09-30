# BMI Calculator

This is a simple **BMI Calculator** built using **Nextjs**. The application allows users to input their height and weight to calculate their Body Mass Index (BMI). Based on the BMI, it classifies the user into a category (Underweight, Normal, Overweight, or Obese) and provides a health recommendation.


## Live Demo

 You can  view the live demo of the application by clicking on this link: [BMI Calculator](https://bmi-calculator-app-8pop.vercel.app/)



## Features

- Input fields for height (in cm) and weight (in kg)
- Calculates BMI and displays the result
- Classifies the user into one of four categories:
  - Underweight
  - Normal
  - Overweight
  - Obese
- Provides health advice based on the BMI category
- Error handling for invalid inputs (empty fields, non-positive numbers)

## Technologies Used

- **React** (with functional components)
- **TypeScript**
- **Tailwind CSS** for styling

## Components

### 1. `BmiCalculator`
This is the main component that renders the entire BMI calculator. It contains:
- State hooks for managing user inputs (`height`, `weight`), the BMI result, and error messages.
- A function (`calculateBmi`) that calculates the BMI based on user input, determines the BMI category, and retrieves health recommendations.
- Conditional rendering to display the BMI result and any error messages.

### 2. **UI Components**
The following components from the UI library are used:
- `Card`: The main card component to encapsulate the BMI calculator.
- `CardHeader`, `CardTitle`, `CardDescription`: Components for the header section.
- `CardContent`: Wraps the main content.
- `Label`: Labels for the input fields.
- `Input`: Input fields for height and weight.
- `Button`: Button to trigger BMI calculation.

## Getting Started

### Usage

1. Enter your height in centimeters in the "Height" input field.
2. Enter your weight in kilograms in the "Weight" input field.
3. Click on the **Calculate** button to see your BMI result.
4. The app will display your BMI value, the corresponding category, and a health recommendation.

### Example

- **Height**: 170 cm
- **Weight**: 65 kg
- **BMI**: 22.5
- **Category**: Normal
- **Health Recommendation**: "Maintain your healthy weight through a balanced diet and regular physical activity."


## Error Handling

If the user tries to calculate BMI without entering both height and weight, an error message will appear:

- **Error Message**: "Please enter both height and weight."
- **Invalid Height or Weight**: If the height or weight is not a positive number, an appropriate error message will display:
  - "Height must be a positive number."
  - "Weight must be a positive number."

## Customization

You can customize the health recommendations in the `healthRecommendations` object located in the `BmiCalculator` component. Modify the advice based on your requirements.

```typescript
const healthRecommendations: { [key: string]: string } = {
  Underweight: "Your custom advice for underweight category",
  Normal: "Your custom advice for normal category",
  Overweight: "Your custom advice for overweight category",
  Obese: "Your custom advice for obese category",
};
```
