FROM busybox AS basis
RUN echo hello > /newfile && chown 123:456 /newfile
FROM basis
COPY --keep-ownership --from=basis /newfile /newfile_123_456
RUN ls -l /newfile_123_456
