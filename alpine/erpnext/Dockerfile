FROM donysukardi/frappe:latest
MAINTAINER Dony Sukardi <ds@dsds.io>

ARG BRANCH
ENV ERPNEXT_BRANCH $BRANCH

USER $FRAPPE_USER
WORKDIR /home/$FRAPPE_USER/frappe-bench
RUN bench get-app erpnext https://github.com/frappe/erpnext --branch $ERPNEXT_BRANCH

ENTRYPOINT ["docker-entrypoint.sh"]
CMD ["app"]
