FROM amazoncorretto:11

RUN curl -o Archi-Linux64-4.7.1.tgz https://www.archimatetool.com/downloads/4.7.1/Archi-Linux64-4.7.1.tgz \
	&& yum install -y tar Xvfb gtk3 \	
	&& tar -xvzf Archi-Linux64-4.7.1.tgz

VOLUME /arch

CMD Xvfb :99 & \
	export DISPLAY=:99 \
	&& Archi/Archi -application com.archimatetool.commandline.app -consoleLog -nosplash --loadModel /arch/MyModel.archimate --html.createReport /arch/output/MyModel

