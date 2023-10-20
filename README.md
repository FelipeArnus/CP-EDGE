# README - Checkpoint 5

Este é um projeto Arduino que utiliza sensores de temperatura, umidade e luz para monitorar e exibir informações em um display LCD. Além disso, ele é capaz de publicar essas informações em um servidor MQTT para compartilhamento ou processamento remoto. Abaixo estão detalhes importantes sobre o projeto:

## Equipe:

- Felipe Arnus – RM: 550923
- João Pedro Vieira – RM: 99805
- João Pedro Chambrone – RM: 97857
- Vitor Hugo – RM: 97758

## Descrição do Projeto:

Este projeto tem como objetivo criar um sistema de monitoramento ambiental que coleta dados de temperatura, umidade e luz, exibe essas informações em um display LCD e as envia para um servidor MQTT. Ele é adequado para aplicações como monitoramento de condições ambientais em espaços fechados, salas de cultivo, entre outros.

## Componentes Utilizados:

- 1 ESP32 (compatível com as bibliotecas e hardware utilizados)
- 1 Sensor de temperatura e umidade DHT22
- 1 Sensor de luminosidade LDR
- 1 Display LCD
- 3 LEDs (cores: verde, amarelo e vermelho)
- 1 Placa de prototipagem (breadboard)
- 29 fios de conexão
- Acesso a uma rede Wi-Fi para comunicação MQTT

## Funcionamento do Código:

O código monitora os sensores continuamente e realiza as seguintes operações, alternando os itens 1 a 3 cada 2 segundos:

1. **Monitoramento de Umidade:** verifica a umidade do ambiente e exibe-a no LCD. Se a umidade estiver acima de 66%, exibe "Umidade ALTA". Se estiver abaixo de 33%, exibe "Umidade BAIXA". Caso contrário, exibe "Umidade OK".

2. **Monitoramento de Luminosidade:** verifica a luminosidade do ambiente e exibe-a no LCD. Dependendo do valor lido, acende LEDs (verde, amarelo ou vermelho) para indicar o respectivamente(via intensidade) nível de luz.

3. **Monitoramento de Temperatura:** verifica a temperatura do ambiente e exibe-a no LCD. Se a temperatura estiver abaixo de 10°C, exibe "Temp: Baixa". Se estiver acima de 15°C, exibe "Temp: Alta". Caso contrário, exibe "Temp: OK".

4. **Comunicação MQTT:** O projeto utiliza o protocolo MQTT para enviar os dados coletados para um servidor MQTT externo. Isso permite que outros dispositivos recebam e processem essas informações.

## Configuração Wi-Fi e MQTT:

- SSID da rede Wi-Fi: "Wokwi-GUEST"
- Senha da rede Wi-Fi: (em branco)
- Servidor MQTT: "broker.hivemq.com"
- Porta MQTT: 1883

## Simulação:
- https://wokwi.com/projects/378689163018348545

