# Desafio
<img width="795" height="289" alt="image" src="https://github.com/user-attachments/assets/51ef5a6e-8456-4a7e-b1b0-d17cf69794a6" />

## Prompt Facil
Como fazer um jumper na fonte para teste
## Resposta
**Guia**: Como fazer Jumper na Fonte ATX (Teste de Bancada)

Fazer um "jumper" permite ligar a fonte de alimentação sem a necessidade de uma placa-mãe. Isso é ideal para testar o funcionamento básico da unidade ou alimentar periféricos de 12V e 5V de forma isolada.

---

### ⚠️ Medidas de Segurança
1. **Desconecte da tomada:** Sempre insira o jumper com a fonte desligada da rede elétrica.
2. **Carga Mínima:** Evite deixar fontes modernas ligadas por muito tempo sem nenhum componente (como um fan ou HD) conectado, pois isso pode causar instabilidade em alguns modelos.
3. **Não force:** O clipe deve entrar suavemente no conector.

---

### Materiais Necessários
* **Um clipe de papel** (em formato de "U") ou um **pedaço de fio rígido** descascado nas pontas.

---

### Passo a Passo

1.  **Localize o Conector:** Utilize o cabo principal de **24 pinos** (o maior de todos).
2.  **Identifique os Pinos:**
    * **PS_ON (Fio Verde):** É o pino de controle. Geralmente é o **pino 16**.
    * **COM (Fio Preto):** São os pinos de aterramento (GND). Existem vários; os mais comuns para o jumper são os **pinos 15 ou 17** (vizinhos ao verde).
3.  **Insira o Jumper:** Conecte uma ponta do clipe no terminal do fio **Verde** e a outra no fio **Preto** ao lado.
4.  **Teste:** Conecte o cabo de força e ligue a chave (I/O) na traseira da fonte.



---

### Tabela de Referência de Tensões
Se você utilizar um multímetro para medir a saúde da fonte, os valores devem ser aproximadamente:

| Cor do Fio | Tensão Esperada | Função |
| :--- | :--- | :--- |
| **Amarelo** | **+12V** | Alimentação de GPU, Motores e CPU |
| **Vermelho** | **+5V** | Circuitos lógicos e USB |
| **Laranja** | **+3.3V** | Memórias e chipset |
| **Roxo** | **+5VSB** | Standby (sempre ativo se a fonte estiver na tomada) |
| **Cinza** | **Power Good** | Sinal de que as tensões estão estáveis |

---

> **Dica de Diagnóstico:** Se a ventoinha girar e parar logo em seguida, a fonte pode estar detectando um curto-circuito interno ou as tensões estão fora do padrão (proteção de segurança).

## Prompt Dificil
Você é um eletricista que atua ha anos na area alem disso voce agora entrou na area da ti com manunteção em computadores de pequeno e grande porte, me diga como fazer um jumper em uam fonte da marca redragon 400 w com selo 80 plus e aprovada pelo techlab, bivolt. Sou um aluno da faculde de ti com minima erxperiencia em computador, faça um passo a passo de forma muito resumida apenas com palavras chaves e alguns complementos de como fazer o jumper. entregue o resultado em markdown em formato de codigo

## Resposta
###  Procedimento de Jumper: Fonte Redragon 400W (80 Plus/TechLab)
Como eletricista e técnico, reforço: a certificação 80 Plus e o selo TechLab garantem eficiência, mas a pinagem segue o padrão global ATX.
### Preparação Rápida
* **Equipamento:** Clipe de papel em "U" ou fio rígido.
* **Segurança:** Fonte fora da tomada (OFF).
* **Carga:** Conecte um Fan (ventoinha) ou HD antigo em um cabo Molex/SATA para evitar ligar a fonte "no vazio".
### Passo a Passo (Palavras-Chave)
1. **LOCALIZAR:** Identifique o conector principal de 24 pinos.
2. **IDENTIFICAR:** Busque o único fio **VERDE** (PS-ON / Pino 16).
3. **ATERRAMENTO:** Escolha qualquer fio **PRETO** adjacente (COM / Terra / Pino 15 ou 17).
4. **JUMPER:** Insira uma ponta do clipe no terminal **VERDE** e a outra no **PRETO**.
5. **ACIONAR:** Conecte o cabo de força e ligue a chave traseira.
### Resultado esperado
* **VENTOINHA GIRANDO:** Fonte ligada e enviando tensões.
* **VENTOINHA PARADA:** Possível defeito ou proteção de curto ativada.
