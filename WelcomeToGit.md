
# Guía Básica de Git

## **Conceptos Básicos**

- **Repositorio**: Proyecto gestionado por Git (local o remoto).
- **Commit**: Instantánea de los cambios realizados.
- **Branch (rama)**: Línea de desarrollo independiente.
- **Staging Area**: Área intermedia para preparar los cambios antes de un commit.
- **Remote**: Repositorio remoto (como GitHub o GitLab).

---

## **Configuración Inicial**

Antes de comenzar, configura tu nombre y correo electrónico:

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@example.com"

```

---

## **Comandos Esenciales**

### **Crear o Inicializar un Repositorio**

- Iniciar un nuevo repositorio:
    
    ```bash
    git init
    
    ```
    
- Clonar un repositorio existente:
    
    ```bash
    git clone <url_del_repositorio>
    
    ```
    

### **Verificar el Estado del Repositorio**

- Ver el estado actual:
    
    ```bash
    git status
    
    ```
    
- Ver los cambios realizados:
    
    ```bash
    git diff
    
    ```
    

### **Agregar Cambios al Staging Area**

- Agregar un archivo específico:
    
    ```bash
    git add archivo.txt
    
    ```
    
- Agregar todos los cambios:
    
    ```bash
    git add .
    
    ```
    

### **Crear un Commit**

- Realizar un commit con un mensaje:
    
    ```bash
    git commit -m "Mensaje del commit"
    
    ```
    

### **Trabajar con Ramas**

- Crear una nueva rama:
    
    ```bash
    git branch nombre_rama
    
    ```
    
- Cambiar a una rama existente:
    
    ```bash
    git checkout nombre_rama
    
    ```
    
- Crear y cambiar a una nueva rama:
    
    ```bash
    git checkout -b nueva_rama
    
    ```
    
- Listar ramas:
    
    ```bash
    git branch
    
    ```
    

### **Fusionar Ramas**

- Fusionar una rama en la actual:
    
    ```bash
    git merge rama_a_fusionar
    
    ```
    

### **Trabajar con Repositorios Remotos**

- Ver conexiones remotas:
    
    ```bash
    git remote -v
    
    ```
    
- Agregar un repositorio remoto:
    
    ```bash
    git remote add origin <url_del_repositorio>
    
    ```
    
- Subir cambios:
    
    ```bash
    git push origin nombre_rama
    
    ```
    
- Actualizar tu repositorio local:
    
    ```bash
    git pull origin nombre_rama
    
    ```
    

### **Ver el Historial**

- Mostrar el historial de commits:
    
    ```bash
    git log
    
    ```
    
- Mostrar un historial compacto:
    
    ```bash
    git log
    ```
    

### **Revertir Cambios**

- Deshacer cambios no confirmados:
    
    ```bash
    git checkout -- archivo.txt
    
    ```
    
- Quitar un archivo del staging area:
    
    ```bash
    git reset archivo.txt
    
    ```
    
- Revertir a un commit específico:
    
    ```bash
    git revert <id_del_commit>
    
    ```
    

---

## **Flujo Básico de Trabajo**

1. Realiza cambios en tus archivos.
2. Verifica el estado del repositorio:
    
    ```bash
    git status
    
    ```
    
3. Agrega los cambios al staging area:
    
    ```bash
    git add archivo.txt
    
    ```
    
4. Haz un commit para guardar los cambios:
    
    ```bash
    git commit -m "Descripción de los cambios"
    
    ```
    
5. Sube los cambios al repositorio remoto:
    
    ```bash
    git push origin main
    
    ```
    

---

## **Ejemplo Práctico**

1. Crear un nuevo repositorio:
    
    ```bash
    mkdir mi_proyecto
    cd mi_proyecto
    git init
    
    ```
    
2. Crear un archivo:
    
    ```bash
    echo "Hola mundo" > archivo.txt
    
    ```
    
3. Agregar y confirmar cambios:
    
    ```bash
    git add archivo.txt
    git commit -m "Añadir archivo de ejemplo"
    
    ```
    
4. Conectar el repositorio remoto y subir cambios:
    
    ```bash
    git remote add origin <https://github.com/usuario/mi_proyecto.git>
    git push -u origin main
    
    ```