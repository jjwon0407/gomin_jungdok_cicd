#OpenJDK 17 기반 이미지 사용
FROM openjdk:11-jre

#작업 디렉토리 설정
WORKDIR /gomin_jungdok

#JAR 파일 및 설정 파일을 컨테이너로 복사
COPY gdgoc-0.0.1-SNAPSHOT.jar /gomin_jungdok/app.jar
COPY application.properties /app/config/application.properties
COPY .env.properties /gomin_jungdok/

EXPOSE 8080

#컨테이너 실행 명령
ENTRYPOINT ["java", "-jar", "-Dspring.config.location=/gomin_jungdok/config/application.properties", "/gomin_jungdok/app.jar", "--debug"]