<!-- Login.svelte -->
<script>
    // Define any necessary data and functions for your login component
</script>

<main>
    <h2>Login</h2>
    <form>
        <div>
            <label for="username">Username:</label>
            <input type="text" id="username" name="username" />
        </div>
        <div>
            <label for="password">Password:</label>
            <input type="password" id="password" name="password" />
        </div>
        <button type="submit">Login</button>
    </form>
</main>

<style>
    /* Add your login component styles here */
    main {
        text-align: center;
        padding: 2rem;
    }

    h2 {
        font-size: 2rem;
        margin-bottom: 1rem;
    }

    form {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    div {
        margin-bottom: 1rem;
    }

    label {
        font-weight: bold;
    }

    input[type="text"],
    input[type="password"] {
        padding: 0.5rem;
        border: 1px solid #ccc;
        border-radius: 4px;
    }
</style>
