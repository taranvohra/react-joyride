---
icon: dog-leashed
---

# Create a guided tutorial

```bash
yarn add react-joyride
```

#### Step 2: Import and Set Up Joyride

Import React Joyride in your component and set up the tour steps:

```javascript
import React, { useState } from 'react';
import Joyride from 'react-joyride';

const TourComponent = () => {
  const [steps, setSteps] = useState([
    {
      target: '.my-first-step',
      content: 'This is the first step of your tour!',
    },
    {
      target: '.my-other-step',
      content: 'This is another step!',
    },
  ]);

  return <Joyride steps={steps} />;
};

export default TourComponent;
```

#### Step 3: Define Tour Steps

Define the steps by specifying target elements and corresponding content. Use unique class selectors to target elements:

```javascript
const steps = [
  {
    target: '.welcome-step',
    content: 'Welcome to our app!',
  },
  {
    target: '.profile-step',
    content: 'Here is your profile.',
  },
];
```

#### Step 4: Customize Tour Options

Optionally, configure options to customize the tour experience:

```javascript
<Joyride
  steps={steps}
  continuous
  showSkipButton
  styles={{
    options: {
      zIndex: 10000,
    },
  }}
/>
```

#### Step 5: Start the Tour

Place `<TourComponent />` in your app, and ensure targeted components have the specified class names. Run your application to start the tour:

```jsx
function App() {
  return (
    <div className="App">
      <TourComponent />
      <div className="welcome-step">Welcome Content</div>
      <div className="profile-step">Profile Content</div>
    </div>
  );
}
```

Now, you've set up an interactive guided tour in your React app using React Joyride!
