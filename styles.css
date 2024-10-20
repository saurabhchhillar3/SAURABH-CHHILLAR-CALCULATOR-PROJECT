let display = document.getElementById('display');
let historyList = document.getElementById('history-list');
let memory = 0;

document.addEventListener('keydown', function(event) {
    const key = event.key;
    if (!isNaN(key) || ['+', '-', '*', '/'].includes(key)) {
        appendNumber(key);
    } else if (key === 'Enter') {
        calculate();
    } else if (key === 'Backspace') {
        deleteLast();
    } else if (key === 'Escape') {
        clearDisplay();
    }
});

function appendNumber(number) {
    display.value += number;
}

function clearDisplay() {
    display.value = '';
}

function deleteLast() {
    display.value = display.value.slice(0, -1);
}

function calculate() {
    try {
        let result = eval(display.value);
        addToHistory(display.value + ' = ' + result);
        display.value = result;
    } catch (error) {
        display.value = 'Error';
    }
}

function addToHistory(entry) {
    const listItem = document.createElement('li');
    listItem.textContent = entry;
    historyList.appendChild(listItem);
}

function memoryClear() {
    memory = 0;
}

function memoryAdd() {
    memory += parseFloat(display.value) || 0;
}

function memorySubtract() {
    memory -= parseFloat(display.value) || 0;
}

function memoryRecall() {
    display.value += memory;
}
