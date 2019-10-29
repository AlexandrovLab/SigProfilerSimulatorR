#' @title
#'
#' @description
#'
#' @param
#'
#' @return
#'
#' @examples
#'
#' @export SigProfilerSimulatorR

SigProfilerSimulatorR <- function(project, project_path, genome, contexts, exome=NULL, simulations=1, updating=FALSE, bed_file=NULL, overlap=FALSE, gender='female', seqInfo=FALSE, chrom_based=FALSE, seed_file=NULL, spacing=1, noisePoisson=FALSE, noiseAWGN=0, cushion=100, region=NULL){
  os <- reticulate::import("os")
  sys <- reticulate::import("sys")

  sigSim <- reticulate::import("SigProfilerSimulator.SigProfilerSimulator")
  sigSim$SigProfilerSimulator(project, project_path, genome, contexts, exome, as.integer(simulations), updating, bed_file, overlap, gender, seqInfo, chrom_based, seed_file, as.integer(spacing), noisePoisson, as.integer(noiseAWGN), as.integer(cushion), region)
  sys$stdout$flush()
}

#' @export probability
probability <- function(chromosome=NULL, position=NULL, mutation=NULL, context=NULL, genome=NULL, mutation_count=1, mutation_file=NULL, exome=FALSE){
  os <- reticulate::import("os")
  sys <- reticulate::import("sys")
  probs <- reticulate::import("SigProfilerSimulator.SigProfilerSimulator")
  probs$probability(chromosome, position, mutation, context, genome, mutation_count, mutation_file, exome)
  sys$stdout$flush()
}
