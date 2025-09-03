const storyText = document.getElementById("story-text");
const button1 = document.getElementById("button1");
const button2 = document.getElementById("button2");

let storyState = 0;  // Estado da história (0 = início)

const story = [
    {
        text: "Você está em uma floresta escura e misteriosa. O que você faz?",
        options: [
            { text: "Seguir pelo caminho iluminado", nextState: 1 },
            { text: "Entrar na caverna escura", nextState: 2 }
        ]
    },
    {
        text: "Você segue pelo caminho iluminado e encontra uma ponte. O que você faz?",
        options: [
            { text: "Cruzá-la", nextState: 3 },
            { text: "Voltar para a floresta", nextState: 4 }
        ]
    },
    {
        text: "Você entra na caverna e ouve um rugido. O que você faz?",
        options: [
            { text: "Explorar a caverna", nextState: 5 },
            { text: "Sair correndo", nextState: 6 }
        ]
    },
    {
        text: "Você cruzou a ponte e encontrou um tesouro! Você venceu a aventura.",
        options: []
    },
    {
        text: "Você voltou para a floresta e perdeu a oportunidade de encontrar algo interessante.",
        options: []
    },
    {
        text: "Você explora a caverna e encontra um dragão! Você foi derrotado.",
        options: []
    },
    {
        text: "Você correu de volta para a floresta e encontrou um grupo de aventureiros. Você foi salvo.",
        options: []
    }
];

// Função para atualizar o texto e as opções
function updateStory() {
    const currentStory = story[storyState];
    storyText.textContent = currentStory.text;
    
    // Se houver opções, atualize os botões
    if (currentStory.options.length > 0) {
        button1.textContent = currentStory.options[0].text;
        button2.textContent = currentStory.options[1].text;
        
        button1.onclick = () => {
            storyState = currentStory.options[0].nextState;
            updateStory();
        };
        
        button2.onclick = () => {
            storyState = currentStory.options[1].nextState;
            updateStory();
        };
    } else {
        button1.style.display = "none";
        button2.style.display = "none";
    }
}

// Iniciar a história
updateStory();
