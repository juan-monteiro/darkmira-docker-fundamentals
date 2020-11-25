FROM alpine:3.12

EXPOSE 22

RUN apk add --update --no-cache openssh

RUN ssh-keygen -A \
 && sed -i s/#PermitRootLogin.*/PermitRootLogin\ yes/ /etc/ssh/sshd_config \
 && echo "root:dm" | chpasswd

ENTRYPOINT [ "/usr/sbin/sshd", "-D" ]