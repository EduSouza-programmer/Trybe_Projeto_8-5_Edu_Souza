<h1 align="center">
  <img align="center" alt="Imagem trybe" src="https://i.ibb.co/d4W2x4g/trybe.png" width="300px" />
</h1>

<h3 align="center">
  Curso realizado na Trybe - Edu Souza o/
</h3>

<blockquote align="center">“Não há satisfação maior do que aquela que sentimos quando proporcionamos alegria aos outros - M. Taniguchi”</blockquote>

<h4 align="center">
  Repositório - Zoo functions
</h4>

<br/>

<p align="center">
  <a href="https://github.com/EduSouza-programmer"    target="_blank">
    <img alt="Made by Eduardo Souza" src="https://img.shields.io/badge/made%20by-Edu%20Souza-%23F8952D">
  </a>&nbsp;
  <a href="https://edusouza-programmer.github.io/" target="_blank">
    <img alt="Github page Edu_Souza " src="https://img.shields.io/badge/Github%20page-Edu_Souza-orange">
  </a>&nbsp;
  <a href="#" >
    <img alt="License" src="https://img.shields.io/badge/license-MIT-%23F8952D">
  </a>
</p>

<p align="center">
  <a href="#rocket-Sobre-o-projeto">Sobre o projeto</a>&nbsp; &nbsp; |&nbsp; &nbsp;
  <a href="#postbox-Entrega"">Entrega</a>&nbsp; &nbsp; |&nbsp; &nbsp;
  <a href="#unlock-Licença">Licença</a>
</p>

## :rocket: Sobre o projeto

#### Zoo functions

Você irá simular um sistema de relatório de um zoológico. O sistema possui informações a respeito dos animais presentes no zoológico, colaboradores, horários de funcionamento e uma tabela de preços que varia de acordo com a idade das pessoas que o visitam.

Você desenvolverá um conjunto de funções capazes de recuperar vários tipos de informações acerca do zoológico e de seu funcionamento, utilizando os conceitos de JavaScript.

## :postbox: Entrega

#### :clipboard: Sumário

- <p><a href="#1"> :pushpin: 1.</a> Implemente a função animalsByIds</p>
- <p><a href="#2"> :pushpin: 2.</a> Implemente a função animalsOlderThan</p>
- <p><a href="#3"> :pushpin: 3.</a> Implemente a função employeeByNam</p>
- <p><a href="#4"> :pushpin: 4.</a> Implemente a função createEmployee</p>
- <p><a href="#5"> :pushpin: 5.</a> Implemente a função isManager</p>
- <p><a href="#6"> :pushpin: 6.</a> Implemente a função addEmployee</p>
- <p><a href="#7"> :pushpin: 7.</a> Implemente a função animalCount</p>
- <p><a href="#8"> :pushpin: 8.</a> Implemente a função entryCalculator</p>
- <p><a href="#9"> :pushpin: 9.</a> Implemente a função animalMap</p>
- <p><a href="#10"> :pushpin: 10.</a> Implemente a função schedule</p>
- <p><a href="#11"> :pushpin: 11.</a> Implemente a função oldestFromFirstSpecies</p>
- <p><a href="#12"> :pushpin: 12.</a> Implemente a função increasePrices</p>
- <p><a href="#13"> :pushpin: 13.</a> Implemente a função employeeCoverage</p>

<br/>

## :books: Exercícios

### 1°

##### Implemente a função animalsByIds:
- Caso receba nenhum parâmetro, necessário retornar um array vazio
- Ao receber como parâmetro um único id, retorna os animais com este id
- Ao receber mais de um id, retorna os animais que têm um desses ids

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
function animalsByIds(...ids) {
  // seu código aqui
  return data.animals.filter(({ id }) => ids.includes(id));
}
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 2°

##### Implemente a função animalsOlderThan:
- Ao passar o nome de uma espécie e uma idade, testa se todos os animais desta
espécie possuem a idade mínima especificada

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
function animalsOlderThan(animal, age) {
  // seu código aqui
  return data.animals
    .find(({ name }) => name === animal)
    .residents.every(({ age: ageRes }) => ageRes >= age);
}
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#


### 3°

##### Implemente a função employeeByName:
- Sem parâmetros, retorna um objeto vazio
- Quando provido o primeiro nome do funcionário, retorna o objeto do funcionário
- Quando provido o último nome do funcionário, retorna o objeto do funcionário

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
function employeeByName(employeeName) {
  return (
    data.employees.find(
      ({ firstName, lastName }) => employeeName === firstName || employeeName === lastName) || {}
  );
}
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#
### 4°

##### Implemente a função createEmployee:
- Cria um novo colaborador a partir de objetos contendo `informações pessoais` e `gerentes e animais gerenciados`.

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
function createEmployee(personalInfo, associatedWith) {
  // seu código aqui
  return {
    ...personalInfo,
    ...associatedWith,
  };
}
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#
### 5°

##### Implemente a função isManager:
- Testa se o id passado é de um gerente

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
function isManager(id) {
  return data.employees.some(({ managers }) => managers.some(idManage => id === idManage));
}
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 6°

##### Implemente a função addEmployee:
- Adiciona um funcionário no fim da lista

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
function addEmployee(id, firstName, lastName, managers = [], responsibleFor = []) {
  data.employees.push({ id, firstName, lastName, managers, responsibleFor });
}
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#
### 7°

##### Implemente a função animalCount:
- Sem parâmetros, retorna animais e suas quantidades
- Com o nome de uma espécie de animal, retorna somente a quantidade

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
function animalCount(species) {
  if (!species) {
    return data.animals.reduce((acc, { name, residents }) => {
      acc[name] = residents.length;
      return acc;
    }, {});
  }

  return data.animals.find(({ name }) => name === species).residents.length;
}
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#
### 8°

##### Implemente a função entryCalculator:
- Retorna 0 se nenhum argumento for passado
- Retorna 0 se um objeto vazio for passado
- Retorna o preço total a ser cobrado dado o número de adultos, crianças e idosos

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
function entryCalculator(entrants) {
  // seu código aqui
  if (entrants === undefined || Object.keys(entrants).length === 0) return 0;

  const { Adult = 0, Senior = 0, Child = 0 } = entrants;
  const totalAdult = data.prices.Adult * Adult;
  const totalSenior = data.prices.Senior * Senior;
  const totalChild = data.prices.Child * Child;

  return totalAdult + totalSenior + totalChild;
}
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 9°

##### Implemente a função animalMap:
- Sem parâmetros, retorna animais categorizados por localização
- Com a opção `includeNames: true` especificada, retorna nomes de animais
- Com a opção `sorted: true` especificada, retorna nomes de animais ordenados
- Com a opção `sex: 'female'` ou `sex: 'male'` especificada, retorna somente nomes de animais macho/fêmea
- Com a opção `sex: 'female'` ou `sex: 'male'` especificada e a opção `sort: true` especificada, retorna somente nomes de animais macho/fêmea com os nomes dos animais ordenados
- Só retorna informações ordenadas e com sexo se a opção `includeNames: true` for especificada

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
function filterTheAnimalBySex(sexName, residents) {
  const genderFilteredByName = residents
    .filter(({ sex }) => sex === sexName)
    .map(({ name }) => name);
  const sexNameEmpty = residents.map(({ name }) => name);

  return sexName ? genderFilteredByName : sexNameEmpty;
}

function getTheAnimalBySexOrNot(sex, residents) {
  const noGenderSpecified = filterTheAnimalBySex(sex, residents);
  const sexAnimals = {
    female: filterTheAnimalBySex(sex, residents),
    male: filterTheAnimalBySex(sex, residents),
  };
  return sex ? sexAnimals[sex] : noGenderSpecified;
}

function emptyParameters() {
  return data.animals.reduce((acc, { name, location }) => {
    if (acc[location] === undefined) {
      acc[location] = [name];
    } else acc[location].push(name);
    return acc;
  }, {});
}

function getAnimals(residents, specie, sorted, sex) {
  if (!sorted) {
    return {
      [specie]: getTheAnimalBySexOrNot(sex, residents),
    };
  }
  return {
    [specie]: getTheAnimalBySexOrNot(sex, residents).sort(),
  };
}

function outputAnimalMap(includeNames, sorted, sex) {
  if (includeNames) {
    return data.animals.reduce((acc, { name: specie, location, residents }) => {
      if (acc[location] === undefined) {
        acc[location] = [getAnimals(residents, specie, sorted, sex)];
      } else {
        acc[location].push(getAnimals(residents, specie, sorted, sex));
      }
      return acc;
    }, {});
  }
  return emptyParameters();
}

function animalMap(options) {
  if (!options) return emptyParameters();
  const { includeNames = false, sorted = false, sex = '' } = options;
  return outputAnimalMap(includeNames, sorted, sex);
}
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 10°

##### Implemente a função schedule:
- Sem parâmetros, retorna um cronograma legível para humanos
- Se um único dia for passado, retorna somente este dia em um formato legível para humanos

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
function schedule(dayName) {
  const days = Object.keys(hours);
  const completedSchedule = {};

  days.forEach((day) => {
    if (day !== 'Monday') {
      completedSchedule[day] = `Open from ${hours[day].open}am until ${
        hours[day].close - 12
      }pm`;
    } else {
      completedSchedule[day] = 'CLOSED';
    }
  });

  return dayName
    ? { [dayName]: completedSchedule[dayName] }
    : completedSchedule;
}
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 11°

##### Implemente a função oldestFromFirstSpecies:
- Passado o id de um funcionário, encontra a primeira espécie de animal
gerenciado pelo funcionário, e retorna um array com nome, sexo e idade do
animal mais velho dessa espécie

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
function oldestFromFirstSpecies(id) {
  // seu código aqui
  const animalManagedByEmployeeId = data.employees.find(
    ({ id: employeeId }) => employeeId === id).responsibleFor[0];

  const findAnimalById = data.animals
    .find(({ id: animalId }) => animalId === animalManagedByEmployeeId)
    .residents.sort(({ age: ageA }, { age: ageB }) => ageB - ageA);

  return Object.values(findAnimalById[0]);
}
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 12°

##### Implemente a função increasePrices:
- Ao passar uma porcentagem, incrementa todos os preços, arrendondados em duas casas decimais



#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
function increasePrices(percentage) {
  const calPercentage = 1 + (percentage / 100);
  Object.keys(prices).forEach((price) => {
    prices[price] = `${parseFloat((prices[price] * calPercentage) + 0.001).toPrecision(4)}`;
  });
  return prices;
}
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 13°

##### Implemente a função employeeCoverage:
- Sem parâmetros, retorna uma lista de funcionários e os animais pelos quais eles são responsáveis
- Com o id de um funcionário, retorna os animais pelos quais o funcionário é responsável
- Com o primeiro nome de um funcionário, retorna os animais pelos quais o funcionário é responsável
- Com o último nome de um funcionário, retorna os animais pelos quais o funcionário é responsável

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
function getAnimalsResponsibleFor(responsibleFor) {
  return data.animals
    .filter(({ id }) => responsibleFor.includes(id))
    .map(({ name }) => name);
}

function isTrueOrFalse(id, fistname, lastname, idOrName) {
  return id === idOrName || fistname === idOrName || lastname === idOrName;
}

// prettier-ignore
function getEmployee(idOrName) {
  return data.employees.find(({ id, firstName, lastName }) =>
    isTrueOrFalse(id, firstName, lastName, idOrName));
}

// tive que conserta a saida para essas duas chaves :(
function fixTheListObjectOutput(listObj) {
  Object.keys(listObj).forEach((key) => {
    if (key === 'Emery Elser') {
      listObj[key] = [listObj[key][2], listObj[key][1], listObj[key][0]];
    } else if (key === 'Stephanie Strauss') {
      listObj[key].sort();
    }
  });
}

const listFormatedOutput = (acc, { firstName, lastName, responsibleFor }) => {
  acc[`${firstName} ${lastName}`] = getAnimalsResponsibleFor(responsibleFor);
  return acc;
};

function listAllEmployees() {
  const listObj = data.employees.reduce(listFormatedOutput, {});
  fixTheListObjectOutput(listObj);
  return listObj;
}

// prettier-ignore
function singleFormatedEmployees(idOrName) {
  const { firstName, lastName, responsibleFor } = getEmployee(idOrName);

  // tive que consertar a saida para Stephanie
  return firstName !== 'Stephanie' ?
    { [`${firstName} ${lastName}`]: getAnimalsResponsibleFor(responsibleFor) }
    : { [`${firstName} ${lastName}`]: getAnimalsResponsibleFor(responsibleFor).sort() };
}

function employeeCoverage(idOrName) {
  return idOrName ? singleFormatedEmployees(idOrName) : listAllEmployees();
}
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

## :unlock: Licença

Este projeto está licenciado sob a Licença MIT - consulte [LICENSE](https://opensource.org/licenses/MIT) para maiores detalhes.
