# Run this file from the parent directory
# TODO: Update the COPY commands as needed for your repo

FROM gcr.io/deeplearning-platform-release/tf2-gpu.2-7

WORKDIR /

# Installs hypertune library
RUN pip install cloudml-hypertune

# Copies the trainer code to the docker image.
COPY utilities /utilities
COPY hyperparameter_tuner /trainer
COPY images/IAM_Words_train /IAM_Words
# COPY IAM_Words_train /IAM_Words
# COPY IAM_Words_test/IAM_Words

# Sets up the entry point to invoke the trainer.
ENTRYPOINT ["python", "-m", "trainer.task"]

