# On11-TodasEmTech-s6-Introducao-Node
Turma Online 11 - Todas em Tech | Back-end | 2021 | Introdução à API:
HTTP e NodeJS

## Para o lar
Abra o PullRequest Respondendo as seguintes questões:

1) Qual a relação entre os métodos HTTP e o CRUD?

Os métodos HTTP paracem estar ligados ao CRUD, criate -> POST, Read -> GET,  Update -> PUT/PATCH,  Delete -> DELETE. Isso porque as pessoas acabam relacionando um REST diretamente a um CRUD. 
Para que isso não ocorra, devemos respeitar sempre os verbos do HTTP.
PUT e DELETE são compatíveis com navegadores da Web, com o XHR. No entanto, no contexto de formulários HTML, a especificação HTML não os suporta, portanto os navegadores também não.
Embora não seja mapeado canonicamente para uma carta no CRUD, muitas estruturas REST também usam GET / entity / para listar entidades do tipo entidade . GET / entity / id lerá a entidade específica que corresponde ao id .



2) Comente, com exemplos, a diferença entre o PUT e o PATCH.

o método PATCH, aplica modificações parciais a um recurso, quando você não quer mandar o payload completo.
Por exemplo: Eu tenho uma conta bancária mas quero atualizar meu nome nessa conta e todas as outras informações quero manter lá, então eu utilizo o método PATCH. 
Ex2: (/usuario/1234) :

Resultado: {'name': 'João'} 

Enquanto o PUT, permite substituições completas de um documento. Quando utilizamos esse método fica legível que a alteração do dado será com referência a entidade completa.

Ex2: (/usuario/1234)
Resultado: {'id': 1234, 'name': 'Joao', 'idade': 25, 'documento': '123.321.12-X'}


3) Assim como na aula, apresente os dados dos JSONs no console 
    - No colors-rgb.js apresente o nome da cor e o codigo RGB como no exemplo: "gainsboro - rgb(220, 220, 220, 1)"
    - No estados-cidade.js apresente o nome do Estado, a sigla e todas as cidadades, sem arrays aparentes no console
    - No filmes.js apresente titulo, plot, generos e lingua. Genero e lingua devem ser apresentados em arrays no console.

4) Defina o conceito de idempotência e como uma API pode ser idempotente. 
 Tem-se idempotência quando se chama a mesma funcionalidade com o mesmo valor e o resultado é exatamente o mesmo. Se o serviço altera o estado (por exemplo escrevendo no banco de dados), então ele não é idempotente.
 O API pode ser indepontente se uma requisição idêntica pode ser feita uma ou mais vezes em sequencia com o mesmo efeito enqianto deixa o servidor no mesmo estado. 

5) Cite alguns diferentes padrões de projetos de software
Abstract Factory, Factory Method, Singleton.
