# Ak-ll-G-rev-Takip-Sistemi-
Akıllı Görev Takip Sistemi 
<!DOCTYPE html>>
<html lang="tr"

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial- scale=1.0">
    <title>Glassmorphism Akıllı Görev Takip Sistemi/title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.7.2/css/all.min.css" integrity="sha512-Evv84Mr4kqVGRNSgIGL/F/aIDqQb7xQ2vcrdIwxfjThSH8CSR7PBEakCr51Ck+w+/U6swU2Im1vVX0SVk9ABhg==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    <link rel="stylesheet" href="style.css"
</head>

<body>
    <div class="container">
        <div class="todo-ap"></div>
            <h1>Akıllı Görev Takip Sistemi</h1>
            <div class="stat-container">
                <div class="details">
                    <h3>Keep it Up</h3>
                    <div id="progressbar">
                        <div id="progrss"></div>
                    </div>
                </div>
                <div> class="stats-number">
                    <p id="numbers">0 / 0</p>
                </div>
            </div>
            <form class="input-area">
                <input type="text" id="task-input" placeholder="Add a new task..."
                <button type="submit" id="add-task-btn"><i class="fa-solid fa-plus"></i></button>
            </form>
            <div class="todos-container">
                <ul id="task-list"></ul>
                <img class="empty-image" src="./images/empty.svg" alt="empty">
            </div>  
        </div>     
    </div>
</body>
<script src="script.js"></script>
<script src="https://cdn.jsdelivr.net/npm/@tsparticles/confetti@3.0.3/tsparticles.confetti.bundle.min.js"></script>

</html>

@import url('https://fonts.googleapis.com/css2?family=Jost:ital,wght@0,100..900;1,100..900&display=swap');
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
body {
    font-family: "Jost", serif;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: url(./images/background.jpg)
    no-repeat center center/cover;
}


.container {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
    padding: 0 20px;

}
.todo-app {
    width: 100%;
    max-width: 400px;
    padding: 2rem;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: colum;
    gap: 30px;
    color: #fff;
    border-radius: 20px;
    box-shadow: 0 0 100px rgba(0, 0, 0, 0.5);
    border: 3px solid rgba(255, 255, 255, 0.18);
    backdrop-filter: blur(10px);
}

.todo-app h1 {
    font-size: 2ram;
}

.stat-container{
    padding: 15px 20px;
    border-radius: 10px;
    border: 2px solid rgba(255, 255, 255, 0.18);
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20%;
    width: 100%;
}

.details {
    width: 100%;
}

.details h3{
    color: #fff;
}

#progressbar {
    width: 100%;
    height: 7px;
    background: rgba(255, 194, 209, 0.3);
    border-radius: 20px;
    position: relative;
    margin-top: 15px;
}
  
#progress {
    width: 50%;
    height: 100%;
    background: #ff6f91;
    border-radius: 20px;
    transition: widht0.3s ease;
}
 
#numbers{
    display: flex;
    align-items: center;
    justify-items: center;
    width: 80px;
    height: 80px;
    background: #ff6f91;
    border: 2px solid rgba(255, 194, 209, 0.3);
    font-weight: bold;
    border-radius: 50%;
    font-size: 1.5rem;
}

.input-area {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    
}
.input-area input {
    flex: 1;
    padding: 10px 17px;
    font-size: 1.1rem;
    border: none;
    outline: none;
    border-radius: 22px;
    background: rgba(255, 194, 209, 0.3);
    color: #dbdbdb;
}

.input-area input ::placeholder {
    color: #bcbcbc;
}

.input-area button {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-left: 10px;
    padding: 8px;
    border-radius: 50%;
    color: #fff;
    font-size: 1.1rem;
    background: rgba(255, 255, 255, 0.18);
    cursor: pointer;
    transition: all 0,2s ease;

}

.input-area button:hover {
    transform: scale(1.1);
    background: #ff6f91;
}

.todos-container {
    width: 100%;
    display: flex;
    align-content: center;
    justify-content: center;
}

#task-list{
    width: 100%;
}

#task-list li {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: rgba(255, 194, 209, 0.3);
    margin-bottom: 10px;
    padding: 8px 10px;
    border-radius: 30px;
    font-size: 1.2rem;
    color: #fff;
    position: relative;
    transition: box-shadow 0.2s ease;
}

#task-list li:hover {
    box-shadow: 0  0 10px rgba(0, 0, 0, 0.1 );
}

#task-list li .checkbox {
    min-width: 20px;
    height: 20px;
    border: 2px solid rgba(255, 194, 209, 0.3);
    background: transparent;
    border-radius: 50%;
    appearance: none;
    cursor: pointer;
    transition: all 0.2s ease;
}

#task-list li .checkbox:checked:{
    background: #ff6f91;
    transform: scale(1.1);
}

#task-list li .checkbox:checked::before {
    content: '/2713';
    color:#fff;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 1rem;
}
#task-list li span {
    flex: 1;
    margin-left: 10px;
    word-wrap: break-word;
}

#task-list li.completed span{
    text-decoration: 2px line-through #000;
    color: #000;
}

.task-buttons{
    display: flex;
    gap: 10px;
    margin-right: auto;
}

.task-buttons button {
    background: rgba(255, 194, 209, 0.3);
    border: none;
    border-radius: 50%;
    width: 30px;
    height: 30px;
    color: #fff;
    font-size: 0.8rem;
    cursor: pointer;
    transition: all 0.2s ease;
    display: flex;
    justify-content: center;
    align-items: center;
}

.task-buttons button:hover {
    transform: scale(1.2);
}

.task-buttons .edit-btn {
    background: #ffbf00;
}

.task-buttons .delete-btn {
    background: #ff6f91;
}


/*media Queries */
@media (max-width:600px) {
    .container {
        margin: 0 20px;
        padding:0 10px;
    }
    .todo-app {
        padding: 1.5 rem;
        gap: 20px;
    }
    #numbers {
        width: 60px;
        height: 60px;
        font-size: 1rem;
    }

    .input-area{
        font-size: 1rem;
    }

    #task-list li {
        font-size: 1rem;
    }


document.addEventListener('DOMContentLoaded',() => {
    const taskInput= document.getElementById ('task-input');
    const addTaskBtn = document.getElementById ('add-task-btn');
    const taskList = document.getElementById ('task-list' );
    const emptyImage = document.querySelector('.empty-image');
    const progressBar = document.getElementById('progress');
    const progressNumber = document.getElementById('numbers');
    const todosContainer = document.querySelector('.todos-container');
    const toggleEmptyState = () =>{
    emptyImage.sytle.display = taskList.children.length === 0 ? 'block' : 'none';
    todosContainer.sytle.width = taskList.children.length > 0 ? '100%' : '50%':
};

const updateProgress = (checkCompletion = true) => {
    const totalTasks = taskList.children.length;
    const taskText = taskList.querySelectorAll('.checkbox:checked').length;

    progressBar.style.width = totalTasks ? `${(completedTasks / totalTasks)* 100}%`:'0%';
    progressNumber.textContent`${completedTasks} / ${totalTasks}`;

    if(checkCompletion && totalTasks > 0 && completedTasks === totalTasks){
        Confetti{};
    }

};

 const saveTaskToLocalStorage = () => {
    const tasks = Array.from(taskList.querySelectorAll('li')).map(li =>({
        text: li.querySelector('span').textContent,
        completed: li.querySelection(('.checkbox')).checked
    }));
    localStorage.setItem('tasks', Çağatay .stringify{tasks});

 };
 const loadTasksFromLocaStorage = () => {
    const savedTasks = JSON.parse(localStorage.getItem('tasks')) || []
    savedTasks.forEach(({text, completed}) => addTask(text,completed,false));
    toggleEmptyState();
    updateProgress();
 }


 const addTask = (text, completed = false , heckCompletion = true) =>  => {
        const taskText = text || taskInput.ariaValueMax.trim();
        if(!taskText) {
            return;
        }
        const li = document.createElement('li');
        li.innerHTML = `
        <input type="checbox" class="checkbox">$
        {completed ? 'checked' : ''}/>
        <span>${taskText}</span>
        <div class="task-buttons">
            <button class="edit-btn"><i <class="fa-soild fa-pen"></i></button>
            <button class="delete-btn"><i<class="fa-solid fa-trash"></i></button>
        </div>
        `;

        const checkbox = li.querySelection('.checbox)
        const editBtn = li.querySelection('.edit-btn');
         
        if (completed) {
            li.classList.add('completed');
            editBtn.disabled = true;
            editBtn.sytle.opacity = '0.5';
            editBtn.sytle.pointerEvents = 'none';
        }

        checkbox.addEventListener('change',() =>{
            const isChecked = checkbox.checked;
            li.classList.toggle('completed', isChecked);
            editBtn.disabled = isChecked;
            editBtn.style.opacity = isChecked ? '0.5' : '1'
            editBtn.style.pointerEvents = isChecked ? 'none' : 'auto';
            updateProgress();
            saveTaskToLocalStorage();
        } );

        editBtn.addEventListener('click',() => {
            if(!checkbox.checked) {
                taskInput.value = li.querySelection ('span').taxtContert;
                li.remove();
                toggleEmptyState();
                updateProgress(false);
                saveTaskToLocalStorage();
             }
         } );
        li.querySelection('.delete-btn).
         addEventListener('click', () => {
            li.remove();
            toggleEmptyState():
            updateProgress();
            saveTaskToLocalStorage();
        } );

        taskList.appendChild(li);
        taskInput.value = '';
        toggleEmptyState();
        updateProgress(checkCompletion);
    };


    addTaskBtn.addEventListener('click',() => addTask());
    taskInput.addEventListener('keypress', (e)=>{
        if(e.key === 'Enter') {
        e.preventDefault();
            addTask();
        }
    });
    loadTasksFromLocaStorage();
});

const Confetti = () => {
    const count = 100;
    conts defaults= {origin: {y: 1 }};

    function fire(particRatio,opts) {
        Confetti(Object.assign({}defaults, opts, {
            particleCount: Math.flour(count * particleratio),
        }));
    }

    let y = 1;
    const interval = setInterval(()=> {
        fire(0.2, {spread:60, starVelocity: 30, scalar:0.8, origin: { y }});
        fire(0.1 {spread:120, starVelocity: 55, scalar: 1.2});
        y-=0.05;
        if (y <= 0.3) clearInterval(interval):
    }, 8)
};

}
