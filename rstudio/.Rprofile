setHook("rstudio.sessionInit", function(newSession) {
  if (newSession && is.null(rstudioapi::getActiveProject())) {
    proj <- list.files("/workspace", pattern = "[.]Rproj$", full.names = TRUE)
    if (length(proj) > 0) rstudioapi::openProject(proj[1])
  }
}, action = "append")
