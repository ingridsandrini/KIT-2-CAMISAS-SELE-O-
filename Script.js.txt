Script.jslet selected = '';

function selectSize(size) {
  selected = size;
  document.getElementById('selected-size').innerText = "Tamanho selecionado: " + size;
}

function buy() {
  if(selected === '') {
    alert('Escolha um tamanho antes de comprar!');
  } else {
    alert('Você selecionou tamanho ' + selected + '!\nAqui você pode integrar o pagamento.');
    // Aqui você pode colocar o link do pagamento via Pix ou gateway
  }
}

// Cronômetro de 40 minutos
let timer = 40 * 60;
const timeDisplay = document.getElementById('time');

const countdown = setInterval(() => {
  const minutes = Math.floor(timer / 60);
  const seconds = timer % 60;
  timeDisplay.innerText = `${minutes}:${seconds < 10 ? '0' : ''}${seconds}`;
  timer--;
  if(timer < 0) clearInterval(countdown);
}, 1000);
