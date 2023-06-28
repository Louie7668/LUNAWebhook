
```bash
  npm install
```
    
## Installation
Enter your webhook and your port into the config
Port Forward the port if needed
Go to your github repository and in the webhook section enter it like this below

http://ENTER_IP_HERE:ENTER_PORT_HERE/recieve_github


make sure to set the ENTER_IP_HERE:ENTER_PORT_HERE to whatever you configged + your servers ip
```bash
  npm install
  npm run start
```


You could change the actual embed to make it look different it does require quite a bit of know how for js

Also its recommended if your commiting multiple thing with descriptions to push them all seperately as it looks cleaner.
  
## Usage/Examples

```javascript
  commits: [
    {
      id
      tree_id
      distinct
      message
      timestamp
      url
      author: [Object]
      committer: [Object]
      added
      removed
      modified: [Array]
    }
  ],
  head_commit: {
    id
    tree_id
    distinct
    message
    timestamp
    url
    author: {
      name
      email
      username
    },
    committer: {
      name
      email
      username
    },
    added
    removed
    modified
  }
}
```


#preview
[![Screenshot-2023-06-28-032327.png](https://i.postimg.cc/HsVGxcp4/Screenshot-2023-06-28-032327.png)](https://postimg.cc/VdQZZN0d)
