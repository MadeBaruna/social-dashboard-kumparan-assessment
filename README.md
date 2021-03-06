# Social Media Dashboard
A social media dashboard using https://jsonplaceholder.typicode.com (although self-hosted with json-server for CRUD reasons + wrapped with Apollo GraphQL [here](https://github.com/MadeBaruna/jsonplaceholder-graphql))

# Running
### Start local development
The jsonplaceholder-graphql needs to be running first
```
# build and run jsonplaceholder-graphql with Docker
docker build -t jsonplaceholder-graphql github.com/MadeBaruna/jsonplaceholder-graphql
docker run -p 5001:5001 -d jsonplaceholder-graphql

# start the app
git clone https://github.com/MadeBaruna/social-dashboard.git 
cd social-dashboard && yarn
yarn start
```

### Start production build
```
REACT_APP_GRAPHQL_URL={jsonplaceholder-graphql url} yarn build
yarn global add serve
serve -s build
```

# Testing
### Unit Test
``` 
yarn test
```

### End-to-End Test
Make sure to have chrome installed, reset your db.json to initial value in jsonplaceholder-graphql, and start the local development as described above.
```
yarn test-e2e
```
