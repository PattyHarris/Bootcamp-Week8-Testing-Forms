# Testing Forms using React

1. First install the next.js app:
```
npx --use-npm create-next-app@latest testing-forms
```

2. Clean out the index.js file (including the imports at the top of the file).

3. Create a 'Form' component in the new 'components' folder.  Import the 'Form' component in the index.js file.
```
import styles from '../styles/Home.module.css'
import Form from '../components/Form';

export default function Home() {
  return (
    <div className={styles.container}>
      <Form />
    </div>
  )
}

```

4. Add a simple test in the Form component:
```
export default function Form() {
    return <p>Hello</p>
}
```

5.  Add the 'form'' that includes a simple 'input' field and 'onChange' event handler - this updates the 'username' via the useState hook.

6. Add the submit handler which does a POST to /api/form.  Note that the code includes a JSON response handler that is supposed to be removed - the endpoint that is added next does return JSON.

7. To handle the route, add a new file, 'form.js' in the '/pages/api' folder.  Here we added a simple POST handler.
