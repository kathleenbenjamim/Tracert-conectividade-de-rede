# 🧪 LAB - Análise de rota com tracert

## 🎯 Objetivo
Analisar o caminho percorrido pelos pacotes até um destino remoto utilizando o comando tracert.

## 🛠️ Ferramentas
- Prompt de Comando (Windows)
- Conexão com a internet

## ⚙️ Comando utilizado
tracert google.com

## 📊 Resultado obtido
Exemplo de saída:
  1 : 4 ms : 4 ms : 4 ms - 2804:14d:a4ba:8026:6a9e:29ff:fe87:7682
  
  2 : 10 ms : 5 ms : 5 ms - 2804:14d:a4ba:1000::1
  
  3 : 8 ms  : 6 ms : 5 ms - 2804:14d:a400:30::1
  
  4 : 7 ms  : 4 ms : 3 ms - 2804:a8:2:84::6b9
  
  5 :   *   :   *  :   *  -  Esgotado o tempo limite do pedido.
  
  6 : 28 ms : 27 ms : 26 ms - 2804:a8:2:b0::11ca
  
  7 : 27 ms : 27 ms : 25 ms - 2800:3f0:83a2::1
  
  8 : 30 ms : 28 ms : 27 ms - 2001:4860:0:1::73c
  
  9 : 23 ms : 24 ms : 24 ms - 2001:4860:0:1::2ef1
  
 10 : 25 ms : 25 ms : 26 ms - 2800:3f0:4004:802::200e

- Rastreando a rota para google.com [2800:3f0:4004:816::200e]
- O primeiro salto corresponde ao gateway padrão, primeira parada sempre = sua rede
- Os saltos seguintes representam roteadores intermediários da internet.
- O símbolo (*) indica que um roteador não respondeu à requisição ICMP.

## 📚 Conceitos aplicados
- Roteamento
- ICMP
- TTL
- Gateway padrão

## 📸 Evidências
<img width="1244" height="545" alt="image" src="https://github.com/user-attachments/assets/939f1ee9-8dec-4081-b9fd-1c0ba9e34bf7" />

## ✅ Conclusão
O comando tracert mostrou o caminho percorrido até o servidor do Google utilizando IPv6. 
Foi possível identificar os roteadores intermediários, incluindo o gateway padrão no primeiro salto e dispositivos da rede do provedor nos saltos seguintes.
A presença de “*” indica que um dos roteadores não respondeu às requisições ICMP, o que é comum em redes reais.
Tempo de resposta: Quanto menor → melhor / Quanto maior → mais lento
