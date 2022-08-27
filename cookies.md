# What is Role Based Access Control (RBAC)?

Role-based access control (RBAC) restricts network access based on a person's role within an organization and has become one of the main methods for advanced access control. The roles in RBAC refer to the levels of access that employees have to the network.

# Example
Management role scope – it limits what objects the role group is allowed to manage.

Management role group – you can add and remove members.

Management role – these are the types of tasks that can be performed by a specific role group.

Management role assignment – this links a role to a role group.


# Cookies

Cookies are the data stored in the form of key-value pairs that are used to store information about the user on their computer by the websites that the users browse and use it to verify them.

npm install react-cookie

```js
const [cookies, setCookie, removeCookie] = useCookies(['cookie-name']);
```

```js
import React, { useState } from 'react';
import { useCookies } from 'react-cookie';

const App = () => {
   const [name, setName] = useState('');
   const [pwd, setPwd] = useState('');
   const [cookies, setCookie] = useCookies(['user']);

   const handle = () => {
      setCookie('Name', name, { path: '/' });
      setCookie('Password', pwd, { path: '/' });
   };
   return (
      <div className="App">
      <h1>Name of the user:</h1>
      <input
         placeholder="name"
         value={name}
         onChange={(e) => setName(e.target.value)}
      />
      <h1>Password of the user:</h1>
      <input
         type="password"
         placeholder="name"
         value={pwd}
         onChange={(e) => setPwd(e.target.value)}
      />
      <div>
         <button onClick={handle}>Set Cookie</button>
      </div>
   </div>
   );
};
export default App;

```
