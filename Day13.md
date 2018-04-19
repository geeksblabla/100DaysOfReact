considering the code below, how would you implement the Repeat Component ?

```jsx
class App extends React.Component {
    constructor() {
        this.request = fetch(`${API_URL}/users`)
        .map(r => r.json());
    }

    render() {
        return withPromise(
            this.request,
            (users) => {
                <React.Fragment>
                    <Repeat foreach={users} as='user'>
                        <UsersListItem />
                    </Repeat>
                </React.Fragment>
            },
            (err) => {
                <React.Fragment>
                    <Text>Error Occured, coundn't fetch the users</Text>
                    <Text>{err}</Text>
                </React.Fragment>
            }
        )
    }
}

const UserListItem({ user }) = (
   ...
);

render(
    <App />
)
```