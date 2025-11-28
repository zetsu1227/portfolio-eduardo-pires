# 🧩 < Fundamentos De Algoritmos >
**Período:** 2025/1  
**Professor:** Lucas Nunes Alegre

---

## 🎯 Problema a ser resolvido
Esta disciplina me ajudou a desenvolver minhas compreensão da lógica básica da construção algorítmica.
Ademais, graças a ela eu dominei as técnicas de decomposição e generalização para a solução de problemas.
Foram propostos vários laborátorios em aula pelos quais tivemos que resolver problemas utilizando a 
linguagem funcional Racket.

---

## 🏗️ Arquitetura e Tecnologias

- Racket como linguagem, sendo ela funcional e procedural
- DrRacket como ambiente de desenvolvimento
- Stepper do DrRacket para verificar o funcionamento do código linha por linha

---

## 🧱 Boas práticas aplicadas

- Formação de contratos dos códigos(objetivo, parâmetros de entrada e saída) 
- Uso de comentário e nomes coerentes nas funções e variáveis
- Identificação dos casos triviais para encerramento de loops e recursões
- Utilização de variáveis locais com o objetivo de diminuir tempo de processamento
- Avaliação do passo-a-passo do código por meio do Stepper

---

## 🤝 Soft Skills e Trabalho em Equipe

- Organização de todos os trechos do código por meio de contratos 
- Manipulação de versões do código dados pelo professor

---

## 🧪 Exemplos de Código
```racket
;; sierpinski: Número Color -> Imagem
;; Obj: Dados o tamanho do lado e uma cor, desenha um triângulo de Sierpinski
;; desta cor cujo lado do triângulo externo é o lado passado como argumento.

(define (sierpinski lado cor);; Dados um lado e uma cor 
  (cond
       ;; se o lado for muito pequeno, desenhar um triângulo com o lado dado
       [(<= lado 5)  (desenha-triangulo lado cor)]
       ;; senão
       ;;      desenha um triângulo de sierpinksi com a metade do tamanho do lado
       ;;      e dá o nome de TRIANGULO para este desenho:
       [else (local
               (
                (define TRIANGULO (sierpinski (/ lado 2) cor))
               )
                ;; e monta a imagem do triângulo de sierpinski colocando um TRIANGULO
                ;; acima de dois outros TRIANGULOs, lado a lado:
               (above TRIANGULO
                      (beside TRIANGULO TRIANGULO)))]))
```

---

## 📈 Resultados e Aprendizados
- O que funcionou bem:  
  1. A abordagem de decompor grandes problemas em menores facilitou a resolução deles.
  2. O uso de contratos tornou o código mais organizado, evitando erros de compreensão da entrada e da saída.
  3. Os exercícios propostos em laboratório fortaleceram o raciocínio lógico e o pensamento algorítmico.
  
- O que poderia melhorar:
  1. Identificar e usar algoritmos que evitam o uso excessivo de recursões.
  
- Conceitos mais aplicados da disciplina:  
  1. Decomposição e generalização de problemas.
  2. Recursão e casos triviais.
  3. Contratos e documentação para definir o comportamento das funções.
  4. Avaliação do fluxo de execução para depuração e entendimento do programa.

- Lições para projetos futuros:  
  1. Criar contratos detalhados desde o início para prevenir erros de lógica.
  2. Priorizar soluções gerais e reutilizáveis ao invés de algo específico para poucos/um casos.
  
