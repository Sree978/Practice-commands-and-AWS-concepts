1. how do u check container logs : docker logs cont-name (2 months) ---->
2. how do u check live resource usage of container (cpu & mem) : docker stats cont
3. copy files from one cont to another container : docker cp cont-name:source-file-path cont:path
4. containers, images, n/w & volumes : 100 GB ---> docker system df
5. how do u get a full info about a n/w : docker inspect n/w n/w-name
6. docker exec -it cont-name <command>
7. docker exec -it cont-name bash
8. how do you remove a container when it wents exited state : docker run --rm image
9. how do u display the config of a compose file : docker-compose config
10. how do u remove a container along with the ass volume : docker rm -v cont-name
11. docker export cont-name flm.tar    -> to back up

Scenario based 

1) its taking more time for scanning,oush & pull container images
-> when image size is huge
    1.1 > multistage dockerfile
    1.2 > baseiamges like : alpine or slim
    1.3 > .dockerignore (to ignore unwanted 
    1.4 > --production or --build-cache
2) what you will do if container exited state
    2.1 > docker logs cont-name
    2.2 > CMD or ENTRYPOINT
    2.3 > missing dependencies
    2.4 > .env variables
3) if conatiner consumes more than we expected howcan you fix it
    3.1 > docker stats cont-name    ->to check memory use
    3.2 > check for memory leaks > to check unwanted files  will use ( Data dog , grafana, prometheous )
    3.3 > limits 
4) conatiner is not running state even its created 
    4.1 > Dockerfile
    4.2 > docker events
    4.3 > enough resources
    4.4 > -it       -> we have to create conatiner in interactive terminal 
5) container created but application ot working
    5.1 > logs
    5.2 > health check 
    5.3 > n/w
    5.4 > restart the container
6) Conatiner life cycle
      <img width="606" height="471" alt="image" src="https://github.com/user-attachments/assets/1ce3a038-6585-450a-8ecf-929df31426a4" />


7) What is container :
    Containers are used to run the applications
    it contains our applications and dependencies
    These are standalone, lite weight and executable unit of s/w that inclused everything for run application

8) what is Docker Image
     Its blueprint or template for create container

9) Diff b/w conatiner & image

Image will define what we need to run the appplication
  Dockerfile : we are mentioning tools, files commands for run the application
iamges are static ( we can't modify images)
Container ( we can modify here )

10) Docker architecture

![Uploading image.png…]()


12) CMD vs ENTRYPOINT

  both will use to run commands while creating conatiners
  the values which you provided in CMd is overwritten whie creating container
  the values which you provided in ENTRYPOINT, we can't overwritten whie creating container

  CMD behaves default 
  ENTRYPOINT to fixed behaviour 
ENTRYPOINT ["python"]    --> Fixed values we can't able to change
CMD ["index.py"]      --> We can change values inside the command

12) COPY vs ADD

    

13)  how to replicates the data from conatiner to conatiner
    by using volumes
   Types : bind , named, unname
    will do it two ways : cmd & dockefile
 
15)  
  



  
   
  







