
 -------------------------------------------------------------------------------------------------------------------------------
 
 FIAP - MBA Arquitetura de Soluções - ASO6
 
-------------------------------------------------------------------------------------------------------------------------------
 
 Grupo 1 - ASO6
 
    RM 341515 - Adriana Akemi Kira
 
    RM 340522 - Bruno Galletti Souza
 
    RM 341648 - Daniel Machado Reis
 
-------------------------------------------------------------------------------------------------------------------------------
 
 Solution Sprint - Fase 4 - CONTAINERIZATION STRATEGY
 
 Blog Deplyment
 
 Full Deplyment YAML
 
-------------------------------------------------------------------------------------------------------------------------------
 
 
-------------------------------------------------------------------------------------------------------------------------------
 
 Conteído do Deployment:

1 - Database - Secret : blog-db-fiap-aso-g1-secret

2 - Database - Persistent Volume Claims (PVC) : blog-db-fiap-aso-g1-pvc

3 - Database - Deplyment (PostgreSQL) : blog-db-fiap-aso-g1

4 - Database - Service :  blog-db-fiap-aso-g1-service

5 - Application - Secret : blog-app-fiap-aso-g1-config-map

6 - Application - Deplyment (blog-django-py) : blog-app-fiap-aso-g1

7 - Applciation - Service : blog-app-fiap-aso-g1-service

8 - Applciation - Route : blog-app-fiap-aso-g1-route

9. Application - Horizontal Pod Autoscalers (HPA) :  blog-app-fiap-aso-g1-hpa


-------------------------------------------------------------------------------------------------------------------------------

-------------------------------------------------------------------------------------------------------------------------------
  Execução do deployment

      executar arquivo: 
       full_deployment.yaml

 -------------------------------------------------------------------------------------------------------------------------------

 -------------------------------------------------------------------------------------------------------------------------------
  Instruções para criar usuario e senha na aplicação:
 
1. Acessar terminal do POD do deplyment "log-app-fiap-aso-g1"

       Exemplo   oc rsh $POD

2. No terminal executar os comandos:

       cp .s2i/action_hooks/setup .
      
       ./setup 	

3. Seguir as intruções do terminal para criação do usuário. Exemplo

             -----> Running Django database table migrations.
            Operations to perform:
              Apply all migrations: admin, auth, blog, contenttypes, sessions
              Running migrations:
              No migrations to apply.
             -----> Running Django super user creation
             Username (leave blank to use '1001880000'): fiap
             Email address: fiap@fiap.com
             Password: 
             Password (again): 
             Superuser created successfully.
             -----> Pre-loading Django database with blog posts.
             Installed 2 object(s) from 1 fixture(s)

-------------------------------------------------------------------------------------------------------------------------------

 	
 	
