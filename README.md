Este programa es una aplicación Java que se conecta a una base de datos PostgreSQL para mostrar información sobre constructores y conductores de Fórmula 1 en una interfaz gráfica. La aplicación utiliza JDBC para la conexión a la base de datos y Swing para la interfaz gráfica de usuario. Aquí hay un desglose de sus componentes principales:

Conexión a la Base de Datos:

El método connectDB() establece la conexión a la base de datos PostgreSQL usando las credenciales y URL proporcionadas.
Se maneja cualquier excepción de SQL para asegurar que se notifique al usuario si la conexión falla.
Interfaz Gráfica de Usuario (GUI):

El método createGUI() configura la ventana principal (JFrame) y su contenido.
La ventana incluye un JComboBox que permite al usuario seleccionar qué tabla desea visualizar: Constructores, Conductores, o ambos.
Un JTable se utiliza para mostrar los datos recuperados de la base de datos.
Actualización de la Tabla:

El método updateTable(String selectedTable) ejecuta una consulta SQL basada en la selección del usuario en el JComboBox.
Dependiendo de la selección, se ejecuta una consulta específica para constructores, conductores, o ambos.
Los resultados de la consulta se cargan en un DefaultTableModel que se utiliza para poblar el JTable.
Limpieza de la Tabla:

El método clearTable() se asegura de que la tabla se vacíe cuando no se selecciona ninguna opción en el JComboBox.
Centrado del Título de la Ventana:

El método centerTitle(JFrame frame, String title) ajusta el título de la ventana para que esté centrado, proporcionando una apariencia más estética.
Método Principal:

El método main lanza la aplicación de manera segura utilizando SwingUtilities.invokeLater.
Esta estructura modular permite mantener una separación clara entre la lógica de conexión a la base de datos, la manipulación de datos y la presentación gráfica, facilitando la mantenibilidad y la escalabilidad de la aplicación.

Tabla constructores:
![image](https://github.com/Braddo05/F1DriversAndConstructs/assets/169103197/7da3e13c-7e0c-4e8b-864a-13de3e7f85a8)
Tabla Drivers:
![image](https://github.com/Braddo05/F1DriversAndConstructs/assets/169103197/76feb144-260c-47bb-87e6-20012133e2a0)
Tabla Drivers Y Constructores:
![image](https://github.com/Braddo05/F1DriversAndConstructs/assets/169103197/7e26fed5-1e93-4ee9-bdd1-d695c6f45b38)
