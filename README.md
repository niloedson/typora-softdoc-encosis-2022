<img src="./figures/typora-review.png" style="zoom:80%" />

# XI Encontro de Computação e Sistemas de Informação - ENCOSIS 2022



## Dia 1 | Mini-curso:

### Usando Typora no auxílio de documentação de software

O Typora é uma ferramenta simples e poderosa que auxilia no processo de documentação de software, aumentando a produtividade do desenvolvedor e a velocidade de edição de Markdowns. Ele remove a necessidade da janela de visualização, o alternador de modo, os símbolos de sintaxe do código fonte Markdown e todas as outras distrações desnecessárias. Em vez disso, ele fornece um recurso de visualização automática para ajudar o desenvolvedor a se concentrar apenas no conteúdo em si da documentação. Além disso, ainda incorpora várias tecnologias que incrementam o arsenal do desenvolvedor para melhorar a elaboração da explicação de seu software.

**Instrutor: Nilo Edson**

<img src="./figures/linkedin-logo.png" style="zoom:3%"/> [/nedson/](https://www.linkedin.com/in/nedson/)






### Objetivos

1. Mostrar as funcionalidades e recursos do Typora;
2. Mostrar o processo de documentação em um projeto real;





### Documentação de Software

**Importância:**

- Mito: *"software bem escrito não precisa ser documentado"*
  - Apenas os desenvolvedores possuem o controle do fonte e conhecimento sobre o código;
- **Documentar o software faz parte do desenvolvimento do produto**;
- Do Manifesto das Metodologias Ágeis:
  - `Software funcional > documentação abrangente`;
- **Avaliar e balancear o peso da importância da documentação**;





### Conteúdo de um projeto

```
repo / Project
	- <source code>
	- <platform dependent files>
	- <optional license files>
	- README.md
```

- `README.md` - Arquivo de documentação escrito em **Markdown**.





### Funcionalidades do Typora

* Referência *Markdown* oficial da ferramenta ([link](https://support.typora.io/Markdown-Reference/))

```
  Preview automático
+ atalhos no teclado
+ uso de temas customizados
+ exportação para PDF e HTML
```

Exportação para outros formatos (Word, OpenOffice, RTF, Epub, LaTeX e etc...) usando o [Pandoc](https://github.com/jgm/pandoc).

``` 
``` <Enter>
```

```
```





### Inserir tags HTML

```html
<div>
    <h1>
        Header 1
    </h1>
    <h2>
        Header 2
    </h2>
    <a>texto</a>
</div>
```

<div>
    <h1>
        Header 1
    </h1>
    <h2>
        Header 2
    </h2>
    <a>texto</a>
</div>





### Criar hyperlinks

```
[ENCOSIS 2022](https://doity.com.br/encosis2022)
<https://doity.com.br/encosis2022>
<a href="https://doity.com.br/encosis2022">ENCOSIS 2022</a>
```

[ENCOSIS 2022](https://doity.com.br/encosis2022)
<https://doity.com.br/encosis2022>
<a href="https://doity.com.br/encosis2022">ENCOSIS 2022</a>





### Estilos na linha

```
Vários estilos suportados: como **negrito**, *itálico*, `código`, emoji :smile:, ~~tachado~~, <u>sublinhado</u>, <mark>realce</mark> e etc.

---

> citação
```

Vários estilos suportados: como **negrito**, *itálico*, `código`, emoji :smile:, ~~tachado~~, <u>sublinhado</u>, <mark>realce</mark> e etc.

---

> citação





### Inserir imagens

```
![logo](./figures/fucapi-logo.jpg)
```

![logo](./figures/fucapi-logo.jpg)



```
<img src="./figures/fucapi-logo.jpg" style="zoom:80%;"/>
```

<img src="./figures/fucapi-logo.jpg" style="zoom:80%;"/>





### *Code fences*

- `C`:

````
``` c
#include <stdio.h>
void foo() {
    printf("Hello ENCOSIS 2022!\n");
}
```
````

``` c
#include <stdio.h>
void foo() {
    printf("Hello ENCOSIS 2022!\n");
}
```



- `Python`:

````
``` python
def foo():
    print("Hello ENCOSIS 2022!\n")
```
````

``` python
def foo():
    print("Hello ENCOSIS 2022!\n")
```





### Tabelas

```
| Version  | Date          | Description   | Author | Email   |
| -------- | ------------- | ------------- | ------ | ------- |
| 0.000001 | April 08, 2022 | First release | Me     | mail@me |
```

| Version  | Date           | Description   | Author | Email   |
| -------- | -------------- | ------------- | ------ | ------- |
| 0.000001 | April 08, 2022 | First release | Me     | mail@me |





### Listas

```
* item 1
- item 2
3. item 3
- [x] check
```

* item 1
- item 2
3. item 3
- [x] check



### Funções matemáticas

```
$$
x^n + y^n = z^n
$$
```

$$
x^n + y^n = z^n
$$



```latex
$$
\sqrt{x^2+1}
$$
```

$$
\sqrt{x^2+1}
$$





### Temas

* Temas disponíveis no próprio site ([link](https://theme.typora.com.cn/));
* Customização de temas também é possível ([link](https://theme.typora.com.cn/doc/Write-Custom-Theme/));





### O Mermaid no Typora

* **Permite criar diagramas e visualizações usando texto e código** ([link](https://mermaid-js.github.io/mermaid/#/README));
* Reduz o tempo, esforço e ferramentas necessárias para criar diagramas e gráficos modificáveis, resultando em conteúdo mais **inteligente** e **reutilizável**;
* Como uma **ferramenta de diagramação baseada em texto**, permite atualizações rápidas e torna a documentação muito mais fácil;
* Também pode ser incluído em **scripts de produção** e outras peças de código conforme requisito;





### Fluxogramas

- Sintaxe básica ([link](https://mermaid-js.github.io/mermaid/#/./flowchart?id=flowcharts-basic-syntax));

````
``` mermaid
graph TD
	A(A:texto) --> B
	A -.-> C
	B([B:texto]) ==> D
	C[(C:texto)] --- D[D:texto]
```
````

``` mermaid
graph TD
	A(A:texto) --> B
	A -.-> C
	B([B:texto]) ==> D
	C[(C:texto)] --- D[D:texto]
```





### Diagramas de sequência

- Sintaxe básica ([link](https://mermaid-js.github.io/mermaid/#/./sequenceDiagram));

````
``` mermaid
sequenceDiagram

activate STM32
STM32->>+ESP8266: AT Command
ESP8266->>-STM32: AT Response
STM32-->>+IRQ: IRQ Handler
deactivate STM32
IRQ-->>-STM32: sets feedback
```
````

``` mermaid
sequenceDiagram

activate STM32
STM32->>+ESP8266: AT Command
ESP8266->>-STM32: AT Response
STM32-->>+IRQ: IRQ Handler
deactivate STM32
IRQ-->>-STM32: sets feedback
```





### Diagrama de estados

- Sintaxe básica ([link](https://mermaid-js.github.io/mermaid/#/stateDiagram));

````
``` mermaid
stateDiagram

[*] --> WAKEUP
WAKEUP --> TEST : OK
TEST --> CONFIG : OK
CONFIG --> CWSTATE?
CWSTATE? --> WIFI : NOT_STARTED or DISCONNECTED
CWSTATE? --> MQTT : CONNECTED_GOT_IP or OK
WIFI --> MQTT : OK
MQTT --> WIFI : ERROR
MQTT --> CONFIG : CRITICAL ERROR
MQTT --> LOOP : OK
LOOP --> CONFIG : RECONFIGURE CONNECTION
LOOP --> TEST : AT INTERFACE ERROR
```
````

``` mermaid
stateDiagram

[*] --> WAKEUP
WAKEUP --> TEST : OK
TEST --> CONFIG : OK
CONFIG --> CWSTATE?
CWSTATE? --> WIFI : NOT_STARTED or DISCONNECTED
CWSTATE? --> MQTT : CONNECTED_GOT_IP or OK
WIFI --> MQTT : OK
MQTT --> WIFI : ERROR
MQTT --> CONFIG : CRITICAL ERROR
MQTT --> LOOP : OK
LOOP --> CONFIG : RECONFIGURE CONNECTION
LOOP --> TEST : AT INTERFACE ERROR
```





### Diagrama de Gantt

- Sintaxe básica ([link](https://mermaid-js.github.io/mermaid/#/./gantt));

````
``` mermaid
gantt
	title Ano Ideal
	dateFormat YYYY-MM-DD
	section Trabalho
	Projeto 1: a1, 2022-04-01, 110d
	Projeto 2: a2, after a1, 110d
	Projeto 3: a3, after a2, 110d
	section Férias
	Férias: b1, after a3, 30d
```
````

``` mermaid
gantt
	title Ano Ideal
	dateFormat YYYY-MM-DD
	section Trabalho
	Projeto 1: a1, 2022-04-01, 110d
	Projeto 2: a2, after a1, 110d
	Projeto 3: a3, after a2, 110d
	section Férias
	Férias: b1, after a3, 30d
```





### Diagrama de classe

- Sintaxe básica ([link](https://mermaid-js.github.io/mermaid/#/./classDiagram));

````
``` mermaid
classDiagram
	class App_HandleTypeDef
	App_HandleTypeDef: +App_StatusTypeDef status
	App_HandleTypeDef: +App_Params params
	App_HandleTypeDef: +App_Init()
	App_HandleTypeDef: +App_BuildStateMachine()
	App_HandleTypeDef: +App_Main()
	App_HandleTypeDef: +App_DebugLog()
	
	class PCA9546A_HandleTypeDef  {
		+I2C_HandleTypeDef * hi2c
		+uint8_t ctrlreg
		+GPIO_TypeDef * RST_GPIOx
		+uint16_t RST_Pin
		+PCA9546A_Init()
		+PCA9546A_Reset()
		+PCA9546A_SelectChannel()
		+PCA9546A_ChannelStatus()
	}
	
	App_Params <|-- PCA9546A_HandleTypeDef
```
````

``` mermaid
classDiagram
	class App_HandleTypeDef
	App_HandleTypeDef: +App_StatusTypeDef status
	App_HandleTypeDef: +App_Params params
	App_HandleTypeDef: +App_Init()
	App_HandleTypeDef: +App_BuildStateMachine()
	App_HandleTypeDef: +App_Main()
	App_HandleTypeDef: +App_DebugLog()
	
	class PCA9546A_HandleTypeDef  {
		+I2C_HandleTypeDef * hi2c
		+uint8_t ctrlreg
		+GPIO_TypeDef * RST_GPIOx
		+uint16_t RST_Pin
		+PCA9546A_Init()
		+PCA9546A_Reset()
		+PCA9546A_SelectChannel()
		+PCA9546A_ChannelStatus()
	}
	
	App_Params <|-- PCA9546A_HandleTypeDef
```





### Gráfico Git

- Sintaxe básica ([link](https://mermaid-js.github.io/mermaid/#/./gitgraph));

````
``` mermaid
gitGraph:
branch master
commit
branch newbranch
checkout newbranch
commit
checkout master
commit
merge newbranch
```
````

``` mermaid
gitGraph:
branch master
commit
branch newbranch
checkout newbranch
commit
checkout master
commit
merge newbranch
```





---



### Obrigado :smile:!





















<img src="./figures/typora-review.png" style="zoom:80%" />

# XI Encontro de Computação e Sistemas de Informação - ENCOSIS 2022



## Dia 2 | Mini-curso:

### Usando Typora no auxílio de documentação de software

O Typora é uma ferramenta simples e poderosa que auxilia no processo de documentação de software, aumentando a produtividade do desenvolvedor e a velocidade de edição de Markdowns. Ele remove a necessidade da janela de visualização, o alternador de modo, os símbolos de sintaxe do código fonte Markdown e todas as outras distrações desnecessárias. Em vez disso, ele fornece um recurso de visualização automática para ajudar o desenvolvedor a se concentrar apenas no conteúdo em si da documentação. Além disso, ainda incorpora várias tecnologias que incrementam o arsenal do desenvolvedor para melhorar a elaboração da explicação de seu software.

**Instrutor: Nilo Edson**

<img src="./figures/linkedin-logo.png" style="zoom:3%"/> [/nedson/](https://www.linkedin.com/in/nedson/)





### Referências

- AMBLER, Scott W. *"Agile Modeling: Effective Practices for eXtreme Programming and the Unified Process"*. *Capítulo 14*. Wiley, 2002.
- RUPING, Andreas. *"Agile Documentation: A Pattern Guide to Producing Lightweight Documents for Software Projects"*. Wiley, 2003.
- ETTER, Andrew. *"Modern Technical Writing: An Introduction to Software Documentation"*. Kindle, 2019.
- MAYER, Christian. *"The Art of Clean Code: Best Practices to Eliminate Complexity and Simplify Your Life"*. *Capítulo 4*. Kindle, 2022.

<div align="center">
    <img src="./figures/book1.jpg" style="zoom:40%"/>
    <img src="./figures/book2.jpg" style="zoom:55%"/>
    <img src="./figures/book3.jpg" style="zoom:45%"/>
    <img src="./figures/book4.jpg" style="zoom:42%"/>
</div>






### Do Manifesto Ágil

| Esquerda                    | >    | Direita                                |
| --------------------------- | ---- | -------------------------------------- |
| **Indivíduos e Interações** | >    | <mark>Processos e Ferramentas</mark>   |
| **Software funcional**      | >    | <mark>Documentação compreensiva</mark> |
| **Colaboração do cliente**  | >    | Negociação por contrato                |
| **Resposta à mudança**      | >    | Seguir um plano                        |





### Documentação Ágil

```mermaid
flowchart TB
source -- contém --> soft
model[Modelo] -- talvez se torne ou faça parte de --> docs[Documento]
model -- talvez descreva --> source[Código Fonte]
docs -- é --> soft[Documentação]
soft -- descreve --> source
```





### Clean Code como Documentação

**Alguns princípios básicos:**

1. Pense nos elementos do projeto como grandes blocos;
2. Escreva código para pessoas, não máquinas;
3. Siga padrões de estilo e seja consistente;
4. Use comentários de forma inteligente;
5. Evite surpresas, implemente o que se espera que aconteça;
6. Princípios da responsabilidade única e do menor conhecimento;
7. Desenvolva testes, mas procure facilitá-los.



---



**Módulo LoRaWAN EndDevice da Radioenge:**



<div align="center">
    <img src="./figures/modulo-lorawan-radioenge.jpg" style="zoom:55%"/>
    <img src="./figures/radioenge-logo.png" style="zoom:20%"/>
</div>




```
TXD:-----------------------AT\r\n--------------------------------------
    <preparação do comando>      <processamento da resposta>
RXD:--------------------------------------------------------AT_OK\r\n--
```




---



<img src="./figures/use-comments.png" style="zoom:75%" />



---



```c++
/**
 * @brief Set datarate to be used by the End Device.
 * 
 * @param datarate identifier
 * @return LoRaWAN::eStatus 
 */
LoRaWAN::eStatus LoRaWAN::setDatarate(LoRaWAN::eDR datarate)
{
    return this->send_AT_DR(datarate, LORAWAN_DEFAULT_TIMEOUT);
}
```



---



### Documentando modelos

**Informações importantes a serem compartilhadas:**

1. Objetivo geral da implementação desenvolvida;
2. Descrição da arquitetura de software utilizada;
3. Princípio básico da funcionalidade dos componentes envolvidos;
4. Dependências utilizadas para o correto funcionamento da solução;
5. Referências utilizadas para o desenvolvimento;
6. Instruções de como expandir as funcionalidades da solução;
7. Referências utilizadas para o desenvolvimento.



---



```mermaid
classDiagram

class LoRaWAN {
	enum eStatus
	enum eBaudrate
	enum eNJM
	enum eCFM
	enum eCLASS
	enum eADR
	enum eDR
	enum NJS
	eStatus checkSerialInterface()
	eStatus setActivationMode()
	eStatus setChannelMask()
	eStatus setPacketDeliveryConfirmation()
	eStatus setDeviceClass()
	eStatus setAdaptiveDatarateConfiguration()
	eStatus setDatarate()
	eStatus setNumberOfRetries()
	eStatus setRX1Delay()
	eStatus setRX2Delay()
	eStatus getDeviceAddress()
	eStatus getNetworkSessionKey()
	eStatus getApplicationSessionKey()
	eStatus checkConnectionStatus()
	eStatus sendString()
	eStatus sendRaw()
}
```



---



```mermaid
sequenceDiagram

Note over LoRaWAN.h, EndDevice : Conexão UART estabelecida corretamente
opt chamada do método
    LoRaWAN.h ->> EndDevice : LoRaWAN::sendAtCommand()
    Note over LoRaWAN.h, EndDevice : envio usando 'polling'

    loop LoRaWAN::waitResponse()
        alt
        	Note over EndDevice : processa comando
            EndDevice ->> LoRaWAN.h : LoRaWAN::huart.readString()
            Note over LoRaWAN.h, EndDevice : recepção usando 'polling'
            Note over LoRaWAN.h : processa resposta
        else
            EndDevice --> LoRaWAN.h : Nenhuma resposta
            Note over LoRaWAN.h : temporizador expira
        end
    end
end
```



---



```c++
LoRaWAN::eStatus LoRaWAN::send_AT_DR(LoRaWAN::eDR datarate, uint32_t timeout)
{
    LoRaWAN::eStatus status;
    String payload = String(datarate);

    status = this->sendAtCommand(AT::DR, AT::SET, payload);

    if (status == LoRaWAN::ERROR) return status;

    status = this->waitResponse(timeout);

    if (status == LoRaWAN::NO_RESPONSE) return status;

    if (!this->buffer.compareTo(_at.getResponse(AT::OK))) return LoRaWAN::OK;

    return LoRaWAN::UNEXPECTED;
}
```



---



### Obrigado :smile:!
