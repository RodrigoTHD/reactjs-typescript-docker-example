# Stage 1: based on Node.js.
FROM node:16.3.0-alpine3.11 as development
# Force sourcemap. Default value: true.
ARG GENERATE_SOURCEMAP=true
# Add a work directory.
WORKDIR /app
# Install dependencies.
COPY package.json .
COPY yarn.lock .
RUN yarn
# Copy app files.
COPY . .
# Expose port
EXPOSE 9090
# Start the app
CMD [ "yarn", "start" ]
