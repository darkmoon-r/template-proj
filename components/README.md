<div align="center">
  <h1>COMPONENTS</h1>
  <p>In this directory, you can store custom components, such as small elements like buttons, progress bars, etc.</p>
</div>

## Example (compoents/Toast/index.js)

    import { memo } from 'react'
    import { ... } from 'react';

    const useStyles = makeStyles((theme) => ({
      root: {
        height: 100,
      },
      ...
    }));

    const Toast = ({ message, toastType, title ... }) => {
      return (
        <div className= ...>
        ...
      );
    };

    export default memo(Toast);

### [Return To Home](../README.md)