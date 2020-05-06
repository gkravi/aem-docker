# Use aem as the base image
FROM aem

# Expose the default port for the publish instance
EXPOSE 4505
COPY ./packages /opt/aem/crx-quickstart/install

# Define the entry command so that this container always start AEM in Publish mode
ENTRYPOINT ["java", "-jar", "cq-quickstart.jar", "-Dsling.run.modes=publish", "-p", "4505"]