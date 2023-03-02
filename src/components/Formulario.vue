
<template>
    
    <div class="flex items-center font-bold ... w-120 rounded overflow-hidden shadow-lg p-12 m-10 snap-start bg-[#fbcfe8]">
      <div class="row">
        <div class="col m12 card-panel">
    
          <form @submit.prevent="agregarUsuario">
              <div class="row">
                <div class="block text-gray-700 text-sm font-bold mb-2" for="username">
                  <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="grid-first-name">
                  
                  Nombre</label>
                  <input class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white" id="grid-first-name" type="text" placeholder="Veronica">
      <p class="text-red-500 text-xs italic">Por favor rellene este campo.</p>
                  
                </div>
                
              </div>
    
            <div class="row">
              <div class="block text-gray-700 text-sm font-bold mb-2" for="username">
                <label>Edad</label>
                <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="username" type="number" v-model="edad">
              </div>
              <div class="block text-gray-700 text-sm font-bold mb-2" for="username">
                <label>Estado Civil</label>
                <select v-model="estado_civil">
                  <option value="">Seleccione</option>
                 
                  <option value="S">Soltero</option>
                  <option value="C">Casado</option>
                  <option value="D">Divorciado</option>
                  <option value="D">Separado</option>
                  <option value="D">Unión libre</option>
                  <option value="V">Viudo</option>
                </select>
              </div>
              <div class="block text-gray-700 text-sm font-bold mb-2" for="username">
                <label>Trabajo</label>
              <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="trabajo" type="text" v-model="trabajo">
              </div>
              <div class="block text-gray-700 text-sm font-bold mb-2" for="username">
                <label>Residencia</label>
              <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="trabajo" type="text" v-model="residencia">
              </div>
              <div class="block text-gray-700 text-sm font-bold mb-2" for="username">
                <label>Cita</label>
              <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="cita" type="text" v-model="cita">
              </div>
              <div class="block text-gray-700 text-sm font-bold mb-2" for="username">
                <label>Cita Autor</label>
              <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="citaAutor" type="text" v-model="citaAutor">
              </div>
              <div class="block text-gray-700 text-sm font-bold mb-2" for="username">
                <label>bio</label>
              <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="bio" type="text" v-model="bio">
              </div>
            </div>
            
            <div class="block text-gray-700 text-sm font-bold mb-2" for="usernames">
              <div class="block text-gray-700 text-sm font-bold mb-2" for="username">
                <label>Personalidad 1</label>
              <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="personalida01" type="text" v-model="personalida01">
              </div>
              <div class="block text-gray-700 text-sm font-bold mb-2" for="username">
                <label>Personalidad 2</label>
              <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="personalida02" type="text" v-model="personalida02">
              </div>
              <div class="block text-gray-700 text-sm font-bold mb-2" for="username">
                <label>Personalidad 3</label>
              <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="personalida03" type="text" v-model="personalida03">
              </div>
              <div class="block text-gray-700 text-sm font-bold mb-2" for="username">
                <label>Personalidad 4</label>
              <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="personalida04" type="text" v-model="personalida04">
              </div>
            </div>

            <div class="block text-gray-700 text-sm font-bold mb-2" for="usernames">
              <form @submit.prevent="agregarObjetivo">
                <div class="col m4 card-panel">
                  <label>Objetivo</label>
                  <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="objetivo" type="text" v-model="objetivo">
                  <button  type="submit" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline">AGREGAR OBJETIVO <i class="material-icons right"></i></button>
                  <br>
                  <ul>
                    <li v-for="objetivo in objetivo" v-bind:key="objetivo">
                        {{objetivo.id}} - {{objetivo.descripcion}}

                    </li>
                  </ul>
                </div>
              </form>
            </div>


            <div class="block text-gray-700 text-sm font-bold mb-2" for="usernames">
              <form @submit.prevent="agregarMotivacion">
                <div class="col m4 card-panel">
                
                  <label>Motivación</label>
                  <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="motivacion" type="text" v-model="motivacion">
                  <div class="block text-gray-700 text-sm font-bold mb-2" for="username">
                <label>Porcentaje</label>
              <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="porcentaje" type="text" v-model="porcentaje">
              </div>
                  <button  type="submit" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline">AGREGAR MOTIVACIÓN <i class="material-icons right"></i></button>
                  <br>
                  
                  <ul>
                    <li v-for="motivacion in motivacion" v-bind:key="motivacion">
                        {{motivacion.id}} - {{motivacion.descripcion}}
                       
                    </li>
                  </ul>
                </div>
              </form>
            </div>

            

            <div class="block text-gray-700 text-sm font-bold mb-2" for="usernames">
              <form @submit.prevent="agregarMarca">
                <div class="col m4 card-panel">
                  <label>Marca</label>
                  <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="marca" type="text" v-model="marca">
                  <button  type="submit" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline">AGREGAR MARCA <i class="material-icons right"></i></button>
                  <br>
                  
                  <ul>
                    <li v-for="marca in motivacion" v-bind:key="marca">
                        {{marca.id}} - {{marca.descripcion}}
                        
                    </li>
                  </ul>
                  
                </div>
                
              </form>
            </div>
            

            <div class="block text-gray-700 text-sm font-bold mb-2" for="usernames">
              <form @submit.prevent="agregarFrustracion">
                <div class="col m4 card-panel">
                  <label>Fustración</label>
                  <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="frustracion" type="text" v-model="frustracion">
                  <button  type="submit" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline">AGREGAR FRUSTACIÓN <i class="material-icons right"></i></button>
                  <br>
                  <ul>
                    <li v-for="marca in frustracion" v-bind:key="marca">
                        {{frustracion.id}} - {{frustracion.descripcion}}
                        
                    </li>
                  </ul>
                </div>
              </form>
            </div>
    
            
    
            <div class="row">
              <button type="submit" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline">AGREGAR<i class="material-icons right"></i></button>
            </div>
          </form> 
        </div>
      </div>
    
      <div class="row">
        <div class="col m12">
          <table class="table bordered striped">
            <thead>
            
            </thead>
            <tbody>
                <tr v-for="usuario in usuarios" v-bind:key="usuario">
                  <td>{{usuario.nombre}}</td>
            
                  <td>{{usuario.edad}}</td>
                  <td>{{usuario.estado_civil}}</td>
                  <td>{{usuario.trabajo}}</td>
                  <td>
                    <ul>
                      <li v-for="personalidad in usuario.pasatiempos" v-bind:key="personalidad">{{personalidad.id}} - {{personalidad.descripcion}}</li>
                    </ul>
                  </td>
                  <td><label><input type="checkbox" disabled v-model="usuario.suscrito"><span></span></label></td>
                  <td><a href="#!"><i class="material-icons">create</i></a></td>
                  <td><a href="#!"><i class="material-icons">delete</i></a></td>
                </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
    
    
    </template>
    
    <script>
    
    export default {
      name: 'App',
      data(){
        return {
          nombre: '',
          edad: 0,
          estado_civil: '',
          trabajo: '',
          personalidad: '',
          personalidades: [],
          usuarios: [],
    
          select_instances: []
        }
      },
      mounted()
      {
        var elems = document.querySelectorAll('select');
        this.select_instances = M.FormSelect.init(elems, null);
      },
      methods: {
        agregarUsuario()
        {
          var data = {
            nombre: this.nombre,
          
            edad: this.edad,
            estado_civil: this.estado_civil,
            trabajo: this.trabajo,
            suscrito: this.suscrito,
            personalidades: this.personalidades
          };
          this.usuarios.push(data);
          this.nombre = '';
        
          this.edad = 0;
          this.estado_civil = '';
          this.trabajo = '';
          this.suscrito = false;
          this.personalidad = '';
          this.personalidades = [];
        },
        agregarPasatiempo()
        {
          var total = this.personalidades.length;
          var ultimo = 0;
          if(total > 0)
          {
            ultimo = this.personalidades[total - 1].id;
          }
          var data = {
            id: ultimo + 1,
            descripcion: this.personalidad
          };
          this.personalidades.push(data);
          this.personalidad = '';
        }
      }
    }
    </script>
    
    <style>
    #app {
      font-family: Avenir, Helvetica, Arial, sans-serif;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      text-align: center;
      color: #2c3e50;
      margin-top: 60px;
    }
    </style>