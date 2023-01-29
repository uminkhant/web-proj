# web-projTomcat server setup

Step 1 : context.xml

 <Resource name="jdbc/student" type="javax.sql.DataSource"
    driverClassName="com.mysql.cj.jdbc.Driver"
    url="jdbc:mysql://localhost:3306/student_db"
    username="root"
    password="admin123”/>

Step 2 : server.xml ->lockout realm


				
			<Realm className="org.apache.catalina.realm.DataSourceRealm" dataSourceName="jdbc/student" localDataSource="true" roleNameCol="role" userCredCol="password" userNameCol="name" userRoleTable="member_tbl" userTable="member_tbl"/>
				
