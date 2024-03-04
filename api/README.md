<div align="center">
  <h1>API</h1>
  <p>In this directory, you can store functions and queries designed to retrieve data from the backend.</p>
</div>

## Example (api/queries/userlist.js)

    import { gql } from '@apollo/client';

    const USER_LIST = gql`
      query {
        UserList{
          page
          perPage
          sort
          ...
        }
      }
    `;

    export { USER_LIST };

### [Return](../README.md)