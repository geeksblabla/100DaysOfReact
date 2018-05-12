consider the code below, we'd like to share the name from `ChildComponent` with `Header` and `Footer`
```jsx
class App extends React.PureComponent {
    render() {
        return (
            <React.Fragment>
                <Header />
                <ChildComponent />
                <Footer />
            </React.Fragment>
        )
    } 
}
const Header = ({ name }) => {
    return <div>Hello {name}</div>
}
const Footer = ({ name }) => {
    return <div>Goodbye {name}</div>
}
class ChildComponent extends React.PureComponent {
    constructor(props) {
        super(props)
        this.state = {
            name: ''
        }
    }
    setValue(value) {
        this.setState(
            state => { ...state, name: value }
        )
    }
    render() {
        return (
            <input type='text' onChange={(e) => this.setValue(e.target.value)}/>
        )
    }
}
```