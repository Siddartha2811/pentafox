[assess.txt](https://github.com/user-attachments/files/25043608/assess.txt)
1)const sleep = ms => new Promise(r=>setTimeout(r,ms));

async function getUsers(userIds){
    const results = [];
    
    for(const id of userIds){
        const results = [];
        
        for(const id of userIds){
            const res = await fetch("/users/{id}");
            results.push(await res.json());
            
            await sleep(1000);
        }
        return results;
    }
}

5)function UserProfile({ userId }) {
const [user, setUser] = useState(null);
// PROBLEM: This function is recreated on every render
const fetchUser = async () => {
const res = await fetch(`/api/users/${userId}`);
setUser(await res.json());
};
useEffect(() => {
fetchUser();
}, [userId]); // ESLint demands fetchUser be here
return <div>{user?.name}</div>;
}

8)
const [todos, setTodos] = useState([{id : 1, text :"Walk dog"}, {id:2,text:"Buy milk"}]);
{todos.map((todo) => (
<li key={todo.id}>
<input defaultValue={todo.text} />
<button onClick={() => removeTodo(todo.id)}>Delete</button>
</li>
))}


