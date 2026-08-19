# pc-lopal
Repositório para armazenar os códigos da aula.

# Desafio 1: Versionamento Semântico

Toda biblioteca JavaScript tem sua versão, por exemplo "1.0.0".  
O versionamento semântico segue o padrão **_major.minor.patch_**.  

**Major:** Mudanças grandes que se tornam incompatível com versões anteriores;  
**Minor:** Adição de novas funções/melhorias mantendo a compatibilidade;  
**Patch:** Correção de erros e bugs.  

A versão 1.0.0 indica o lançamento público e estável do projeto.  

Quem decide quando esse número muda são os próprios desenvolvedores, se baseando nas regras acima e no manual oficial do versionamento semântico www.semver.org/lang/pt-BR/.  



# Desafio 2: Dependencies e devDependencies

**Dependencies** são bibliotecas necessárias para executar a versão final do seu código, algo essencial para que seu sistema funcione.  
**DevDependencies** são bibliotecas que servem como uma ferramenta para o programador, rodando apenas enquanto você escreve o código, como o chalk.  
Coloque em **dependencies** bibliotecas nas quais o sistema depende para funcionar. Coloque em **devDependencies** ferramentas que você vai usar na hora de programar.



# Desafios 3: Símbolos ^ e ~ no package.json

No package.json, esses símbolos definem regras de atualização para as versões das dependências, controlando quais atualizações são permitidas ao rodar o `npm install`  
Com o acento circunflexo/caret (^) antes da versão, ao rodar `npm install` apenas a versão minor e patch serão atualizadas. (Se a versão major for 0, apenas a patch será atualizada.)  
Com o til/tilde (~), apenas a versão patch será atualizada.

Sem nenhum símbolo antes da versão, ela não será atualizada automaticamente, se mantendo após a execução do `npm install`.



# Desafios 4: CommonJS e ES Modules (ESM)

O CommonJS e o ESM são sistemas utilizados para organizar e dividir códigos JavaScript em módulos.

### Origens:

O **CommonJS** foi criado em 2009 por Kevin Dangoor com o nome de ServerJS como um padrão para o JavaScript rodar fora de navegadores web, e dividir o código em vários arquivos.  

O **ES Modules** surgiu em 2015 para ser o padrão oficial de divisão de módulos em JavaScript.

### Principais diferenças:

As principais diferenças entre o ESM e o CommonJS são a síntaxe utilizada na importação e exportação de módulos, e a forma de carregamento dos módulos (assíncrono/síncrono).

A síntaxe utilizada pelo CommonJS:

```
// Importação:
const myModule = require('./myModule');
myModule();

// Exportação:
module.exports = function() {
    console.log('Hello from CommonJS!');
  ```

  A síntaxa utilizada pelo ES Modules:

```
// Importação:
import { myModule } from './myModule.js';
myModule();

// Exportação:
export function myModule() {
    console.log('Hello from ES Modules!');
}
```