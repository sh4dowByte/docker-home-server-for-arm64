FROM kalilinux/kali-rolling
 
LABEL maintainer="Ahmad Juhdi <ahmadjuhdi007@gmail.com>"

# RUN apt-get update && apt-get install -y
RUN apt-get update -yqq && \
      apt-get install -yqq \
      curl \
      python3

###########################################################################
# Metasploit
###########################################################################

ARG METASPLOIT=false

RUN if [ ${METASPLOIT} = true ]; then \
    # Install Metasploit
    curl https://raw.githubusercontent.com/rapid7/metasploit-omnibus/master/config/templates/metasploit-framework-wrappers/msfupdate.erb > msfinstall && \
    chmod 755 msfinstall && \
    ./msfinstall \
;fi