# Simulação com o exemplo Human Wolf Sheep

## Apresentação do novo modelo

O modelo Human Wolf Sheep foi desenvolvido com base no exemplo "Wolf Sheep" fornecido no repositório do [framework MESA](https://github.com/projectmesa/mesa-examples). O modelo original
tem por objetivo simular o ecossistema existente entre lobos e ovelhas. Por sua vez, o novo modelo "Human Wolf Sheep" visa simular as consequência da inserção de humanos nesse ecossistema.

## Hipótese

Ao rodar o modelo "Wolf Sheep" algumas vezes, notou-se que caso se tenha as ovelhas sejam extintas antes dos lobos, estes não sobrevivem por muito tempo, pois não se alimentam de grama. 
Caso contrário, as ovelhas sobrevivem bem melhor, pois mantiveram sua fonte de energia e não possuem a ameaça de serem comidas por lobos. Tendo isso em vista, 
foi criado um agente que representa um humano, o qual se alimenta de grama e ovelha, mas que também pode ser comido por lobos, a fim de se analisar a influência que este quarto
elemento exerce perante este ecossistema.

## Mudanças realizadas

-- adicionei o arquivo "mesa_file.py" pois o código não estava conseguindo importar "time" do módulo "mesa.time"
-- adicionei o agente "Human" que representa o ser humana que se alimenta de grama e carne de ovelha, mas que também pode ser atacado por lobos.
- Para tal, foi reproduzido o comportamento do lobo referente a ovelha para codificar o humano também comendo ovelha, o comportamento da ovelha comendo grama para codificar o humano também comendo grama
e o comportamento do lobo ao se mexer foi alterado a fim de se incluir suas ações caso esteja no mesmo quadrado que um humano. 
Os comportamento referentes a reproducibilidade e quantidade de energia adiquirida a partir da alimentação também foram codificados com base nos comportamentos das ovelhas e dos lobos

## Como usar o simulador

Para utilizar o simulador e rodar o novo modelo, basta executar o seguinte comando: "mesa runserver"

## Varíaveis armazenadas no arquivo CSV


\item Deve apresentar uma variação no comportamento do modelo e no comportamento dos agentes. As duas variações podem ser mínimas, mas precisam ser justificadas, baseadas em alguma hipótese causal que você deve declarar, sobre o seu entendimento do modelo que está sendo simulado;
\item Deve permitir que pelo menos um parâmetro ou variável de controle adicional possa ser manipulável na interface do usuário, na parte interativa do modelo. A sua hipótese causal deve estar relacionada com essa variável manipulável;
\item Deve apresentar, na interface de interação com a simulação, algum gráfico mostrando a variação de dados de efeito, necessariamente relacionados com a sua hipótese causal. Podem ser os mesmos dados já existentes na simulação original, ou novos dados que você acha importante serem apresentados;
\item Deve coletar e gravar dados gerados durante cada execução da simulação, em dois arquivos no formato CSV, usando as ferramentas próprias do framework, apresentadas na URL \url{https://mesa.readthedocs.io/en/stable/tutorials/intro_tutorial.html#collecting-data}. Um dos arquivos contém os dados de variáveis no nível do modelo, e outro de variáveis no nível do agente, por exemplo:
{\footnotesize
    \begin{itemize}
        \item \verb|model_data_iter_10_steps_10_2021-11-05 17:32:12.906885.csv|
        \item \verb|agent_data_iter_10_steps_10_2021-11-05 17:32:12.906885.csv|
    \end{itemize}
