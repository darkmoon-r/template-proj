<div align="center">
  <h1>CONTEXTS</h1>
  <p>In this directory, you can store global state management system.</p>
</div>

## Example (contexts/api-context.js)

    import { createContext, useContext } from 'react';
    import { USER_LIST } from 'api/queries/userList';

    const APIContext = createContext(null);

    export function APIProvider({ children }) {

      const getUserList = () => {
        return useQuery(USER_LIST);
      }

      return (
        <APIContext.Provider value={{ getUserList, ... }}>
          {children}
        </APIContext.Provider>
      );
    }

    export function useAPIContext() {
      const context = useContext(APIContext);
      if (!context) {
        throw new Error('Context not initialized yet.');
      }
    
      const { getUserList, ... } = context;

      return { getUserList, ... };
    }

### [Return To Home](../README.md)